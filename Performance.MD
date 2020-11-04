# 性能优化方法（DrawCall）
- 参考地址：[点击进入](https://forum.cocos.org/t/cocos-creator-drawcall/95043)
## 一、静态合图
 - 使用cocoscreator自动图集资源（Auto Atlas）功能进行合图，将同一个文件夹中的散图打包为一个图集，尺寸1024x1024
```
关于自动图集的几点建议
    1:合理控制图集最大尺寸，避免单个图像加载时间过长。
    2:尺寸太大的图像没有必要打进图集（如背景图）。
    3:善用九宫格（Sliced）可以节省很多空间（这一点需要美术大佬配合）。
    4:间距保持默认的2并保持勾选扩边选项，避免图像裁剪错误和出现黑边的情况。
    5:勾选不包含未被引用资源选项，自动排除没有用到的图像以节省空间（该选项预览时无效）。
    6:开发时预览图集，根据结果进行调整，以达到最好的优化效果。
    自动图集资源官方文档：http://docs.cocos.com/creator/manual/zh/asset-workflow/auto-atlas.html#配置自动图集资源
```
 - TexturePacker打包图集
 ### Auto Atlas 和 TexturePacker 的对比
 - Auto Atlas
- - Cocos Creator 内置，方便到家了
- - 功能不多但是该有的都有，免费
- - 项目构建时才生成图集，开发时任意修改无压力
- - 图集尺寸在生成时自适应，节省空间
- - 支持自动纹理压缩
- - TexturePacker
 - 第三方软件需自行安装，不够方便
- - 收费功能很多很专业但是用不着，免费功能也够用
- - 先生成图集再使用，更换图像又要重新生成图集
- - 尺寸固定需要自己设置
- - 自己压缩去
- - 总结：Auto Atlas 真香！
## 二、动态合图（Dynamic Atlas）
- [动态合图官方文档](https://docs.cocos.com/creator/manual/zh/advanced-topics/dynamic-atlas.html)
- 只有纹理开启了 Packable 选项的精灵才能够参与动态合图，该选项默认开启。
```
    动态合图尺寸设置
    cc.dynamicAtlasManager.maxFrameSize = 512;
    强制开启动态合图
    cc.macro.CLEANUP_IMAGE_CACHE = false;
    cc.dynamicAtlasManager.enabled = true;
```
## 三、位图字体（BMFont），并将字体图片打包成图集
- 在场景中使用系统字体或 TTF 字体的 Label 会打断渲染合批，特别是 Label 和 Sprite 层叠交错的情况，每一个 Label 都会打断合批增加一个 DrawCall
## 四、文本缓存模式（Cache Mode）
- [Cache Mode 官方文档](https://docs.cocos.com/creator/manual/zh/components/label.html)
#文本缓存类型（cache-mode）
- - BITMAP  静态文本，例如title,discripting，参与动态合图
- - NONE 默认值，Label 中的整段文本将生成一张位图。会打断渲染批次
- - CHAR 该模式只能用于字体样式和字号固定，并且不会频繁出现巨量未使用过的字符的 Label。因为共享位图的最大尺寸为 2048*2048，占满了之后就没办法再渲染新的字符，需要切换场景才会清除共享位图。
## 五、UI 层级调整
- 例如，将lable和sprite等对象分层管理，不要和label交叉排列
- - 补充
- - - 1:改变渲染状态会打断渲染合批，例如改变纹理状态（预乘、循环模式和过滤模式）或改变 Material（材质）、Blend（混合模式）等等，所以使用自定义 Shader 也会打断合批。

- - - 2:图集默认不参与动态合图，手动开启自动图集资源的 Packable 选项后如果最终图集符合动态合图要求也可以参与动态合图。

- - - 3:纹理开启 Packable 选项参与动态合图后无法使用自定义 Shader，因为动态合图会修改原始贴图的 UV 坐标。

- - - 4:使用 Cache Mode 的 BITMAP 模式需要注意内存情况，CHAR 模式需要注意文本内容是否多且不重复。

## 六、webbp资源
- 将较大的背景图(jpg)转换成webbp格式的资源，大幅降低资源大小
- （通过script_tools中的 webbp打包脚本可实现）