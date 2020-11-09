# 一、扩展编辑器（自定义插件）
## 概念
- Cocos Creator 提供了一系列方法来让用户定制和扩展编辑器的功能。这些扩展以包（package）的形式进行加载。用户通过将自己或第三方开发的扩展包安装到正确的路径进行扩展的加载，根据扩展功能的不同，有时可能会要求用户手动刷新窗口或者重新启动编辑器来完成扩展包的初始化。

- Cocos Creator 的扩展包沿用了 Node.js 社区的包设计方式，通过 package.json 描述文件来定义扩展包的内容和注册信息。
# 本文以脚本绑定插件为例（给当前场景中选中节点直接绑定脚本）
- 功能描述：通过该插件可以一键快速的创建并绑定脚本到场景中选中节点上，相比普通手动创建文件夹创建脚本再拖动脚本到节点上，节省了不少环节和时间，这样更加高效，且模版脚本可以自定义；自定义包含一些默认项目所需的变量函数等，可以更加高效率的开发。
## 1、扩展包的结构大致如下：
```
bindscript
├── main.js             //入口函数
├── moduleScript.ts     //模版脚本
├── package.json        //包描述文件
├── panel               //自定义插件面板
│   ├── index.css       //样式文件
│   ├── index.html      //界面文件
│   └── index.js        //界面入口函数
├── sceneWalker.js      //可以直接访问场景的脚本
```
## 2、工作流程（使用篇）
- 1:将插件放到项目根目录packages文件夹下面
- 2:打开项目工程，选中需要绑定脚本的节点，打开菜单栏脚本绑定插件
- - package.json
``` json
/* 编辑器菜单栏 */
"main-menu": {
    "脚本绑定/打开": {
        /* 调用打开main.js中打开面板方法 */
        "message": "bindscript:opanPanel"
    }
},
```
- - main.js
```javascript
/**
 * 打开面板
 */
opanPanel() {
    Editor.Panel.open("bindscript");
}
```
- 3:填写脚本名字和脚本路径，点击开始
- 4:查看节点上是否已经绑定上指定脚本组件
# 二、文件结构诠释
## 1、入口程序main.js结构
``` javascript
'use strict';
module.exports = {
  load () {
    // 当 package 被正确加载的时候执行
  },

  unload () {
    // 当 package 被正确卸载的时候执行
  },

  //事件（消息）注册监听
  messages: {
    'say-hello' () {
      Editor.log('Hello World!');
    }
  },
};
```
## 2、包描述文件：package.json
``` json
package.json
{
    /* 包名 */
    "name": "bindscript",
    "version": "0.0.2",
    "discription": "bindscript plugin",
    "author": "xusanduo",
    /* 入口函数 */
    "main": "main.js",
    /* 编辑器菜单栏 */
    "main-menu": {
        "脚本绑定/打开": {
            /* 调用打开main.js中打开面板方法 */
            "message": "bindscript:opanPanel"
        }
    },
    /* 字段用于声明一个扩展包内的脚本，在该脚本中可以使用引擎 API，并访问当前场景中的节点和组件。*/
    "scene-script": "sceneWalker.js",
    "panel": {
        /* 面板标题 */
        "title": "操作面板",
        /* 面板的入口函数 */
        "main": "panel/index.js",
        /* 面板类型 */
        "type": "dockable",
        "width": 300,
        "height": 400
    }
}
type 面板类型，可选类型有
    1:dockable：该面板为标准的编辑器面板，可以自由的在编辑器内停靠。
    2:float：该面板为浮动面板，不能停靠在编辑器中。
    3:fixed-size：该面板和浮动面板功能相似，不同之处在于他的窗口大小是固定的。
    4:quick：该面板和浮动面功能相似，不同之处在于当他失去焦点后将会自动关闭。
    5:simple：简单面板拥有独立窗口，通过读取用户自定义的 html 文件展示界面。

```
# 三、进程间的相互调用
- 主进程注册方法要定义在messages对象中
``` javascript
'use strict';
module.exports = {
  //事件（消息）注册监听
  messages: {
    opanPanel () {
      Editor.Panel.open("包名")
      setTimeout(() => {
            Editor.log("-----------1")
            Editor.Ipc.sendToPanel("bindscript", "panelFunc");
        }, 5000);
    }
  },
};
```
- 子进程（如面板主脚本index.js)注册方法要定义在messages对象中
``` javascript
Editor.Panel.extends({
    //...
    messages: {
        panelFunc() {
            Editor.log("main call son");
        }
    }
});
```
- 1:菜单栏调用主进程main.js函数
``` json
"main-menu": {
        "脚本绑定/打开": {
            "message": "包名:函数名" //"message": "bindscript:opanPanel"
        }
    },
```
- 2:打开面板
``` javascript
opanPanel() {
    Editor.Panel.open("包名");//Editor.Panel.open("bindscript");
},
```
- 3:主进程调用子进程（面板）方法
``` javascript
Editor.Ipc.sendToPanel("包名", "函数名");//Editor.Ipc.sendToPanel("bindscript", "panelFunc");
```
- 4:子进程调用主进程方法
``` javascript
Editor.Ipc.sendToMain("包名:函数名", 参数1, 参数2);//Editor.Ipc.sendToMain("bindscript:callSceneScript", 参数1, 参数2);
```
- 5:主进程调用渲染进程（场景脚本）
``` javascript
callSceneScript(event, className, filePath) {
    Editor.Scene.callSceneScript("包名", "函数名", 参数1, 参数2);//Editor.Scene.callSceneScript("bindscript", "getCanvasChildren", className, filePath);
}
```














