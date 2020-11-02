## 一、屏幕适配
#
### 屏幕适配的连个核心配置
- a.设计分辨率：美术设计资源时候的分辨率，也是我们所有资源参考的分辨率，我们就是基于这个分辨率来适配到其他不同的手机分辨率上
- b.适配策略：固定宽度/固定高度
通常横屏游戏适配高度（固定高度），竖屏游戏适配宽度（固定宽度）
游戏中的部件可以通过利用widget设置相对位置（找好参考点）
- c.背景适配可以根据游戏的特点（横竖版），让美术将游戏背景的宽度或者高度做大一些
```
附上一段代码
if (Orientations === "1") {
            canvas.getComponent(cc.Canvas).designResolution = cc.size(640, 1136);
            cc.view.setFrameSize(this.fmsize.height, this.fmsize.width)
            cc.view.setDesignResolutionSize(this.rtsize.height, this.rtsize.width, cc.ResolutionPolicy.SHOW_ALL);
            cc.view.setOrientation(cc.macro.ORIENTATION_PORTRAIT);
        } else {
            canvas.getComponent(cc.Canvas).designResolution = cc.size(1136, 640);
            cc.view.setFrameSize(this.fmsize.width, this.fmsize.height)
            cc.view.setDesignResolutionSize(this.rtsize.width, this.rtsize.height, cc.ResolutionPolicy.SHOW_ALL);
            cc.view.setOrientation(cc.macro.ORIENTATION_LANDSCAPE);
        }
```

## 二、图像渲染
# 
### 将图像显示到屏幕上
### 1、基本图像渲染组件
- sprite,label,mask（mask用于规定子节点可渲染的范围）
### 2、外部资源渲染，基本渲染组件
- ParticaleSystem
TiledMap
Spine
DragonBones
VideoPlayer
WebView
### 3、摄像机
### 4、Material 材质资源
- 材质资源可以用来控制渲染组件在场景中的视觉效果。简单来说材质就是用来指定物体表面的特性，如颜色、光亮程度、自发光度以及不透明度等。




