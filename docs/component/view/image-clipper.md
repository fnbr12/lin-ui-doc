---
title: 图片裁剪 ImageClipper(研发中)
---

# <H2Icon/> 图片裁剪 ImageClipper(研发中)

> 图片裁剪组件。

## 介绍

根据下图所示，`ImageClipper`分为三个区域：`ImageContent`、`ClipperContent`、`Tools`。

该组件默认撑满整个屏幕，您可以通过 `l-class` 外部样式类进行定制。

- `ImageContent`—— 图片内容区域：被裁剪的图片可以在此区域任意移动、放大、缩小和旋转等操作
- `ClipperContent`—— 裁剪内容区域：此区域可以放大缩小，裁剪只会保留该区域的内容
- `Tools`—— Tools区域：在此区域，您可以任意定制您想要的功能，如图所示，可以放一些功能性的按钮，当然，您也可以放其他内容，随心所欲，我们会默认内置一些功能，此区域默认功能需引用子组件 `ImageClipperTools` 


以上三个名词分别对应的部分如下图所示：
<img-wrapper>
<a data-fancybox href="/screenshots/image-clipper/image-clipper.png">
<img  src="/screenshots/image-clipper/image-clipper.png"/>
</a>
</img-wrapper>


## 组件属性（ImageClipper Attributes）

| 参数 | 说明 | 类型 | 可选值 | 默认值 |  
|:----|:----|:----|:----|:----|
| show	| 设置组件展示隐藏	| Boolean | - | false |
| image-url	| 图片路径	| String | - | - |
| type	| 生成图片类型	| String | `base64`  `url` | `url` |
| quality	| 生成图片质量	| Number | 0~1 | 1 |
| width	| 裁剪框宽度，单位为 `rpx`	| Number | - | 400 |
| height	| 裁剪框高度，单位为 `rpx`	| Number | - | 400 |
| min-width	| 裁剪框最小宽度，单位为 `rpx`	| Number | - | 400 |
| min-height	| 裁剪框最小高度，单位为 `rpx`	| Number | - | 400 |
| max-width	| 裁剪框最大宽度，单位为 `rpx`	| Number | - | 400 |
| max-height	| 裁剪框最大高度，单位为 `rpx`	| Number | - | 400 |
| lock-width	| 是否锁定裁剪框宽度	| Boolean | - | false |
| lock-height	| 是否锁定裁剪框高度	| Boolean | - | false |
| lock-ratio	| 是否锁定裁剪框比例	| Boolean | - | false |
| scale-ratio	| 生成图片相对于裁剪框的比例	| Number | - | 1 |
| min-ratio	| 图片最小缩放比	| Number | - | 0.5 |
| max-ratio	| 图片最大缩放比	| Number | - | 2 |
| disable-scale	| 是否禁止缩放	| Boolean | - | false |
| limit-move	| 是否限制移动范围	| Boolean | - | false |

## 组件属性（ImageClipperTools Attributes）

| 参数 | 说明 | 类型 | 可选值 | 默认值 |  
|:----|:----|:----|:----|:----|
| check-image	| 是否显示选择图片按钮	| Boolean | - | true |
| check-image-icon	| 选择图片按钮图标url地址	| String | - | - |
| rotate-along	| 是否显示顺时针旋转按钮	| Boolean | - | true |
| rotate-along-icon	| 顺时针旋转按钮图标url地址	| String | - | - |
| rotate-inverse	| 是否显示逆时针旋转按钮	| Boolean | - | true |
| rotate-inverse-icon	| 逆时针旋转按钮图标url地址	| String | - | - |
| sure	| 是否显示确定按钮	| Boolean | - | true |
| sure-icon	| 确定按钮图标url地址	| String | - | - |
| close	| 是否显示关闭按钮	| Boolean | - | true |
| close-icon	| 关闭按钮图标url地址	| String | - | - |
| lock-width	| 是否显示锁定裁剪框宽度按钮	| Boolean | - | false |
| lock-height	| 是否显示锁定裁剪框高度按钮	| Boolean | - | false |
| lock-ratio	| 是否显示锁定裁剪框比例按钮	| Boolean | - | false |
| disable-scale	| 是否显示禁止缩放按钮	| Boolean | - | false |
| limit-move	| 是否显示限制移动范围按钮	| Boolean | - | false |
| rotate-angle	| 旋转按钮每次旋转的角度	| Number | - | 90 |


## 组件外部样式类（ImageClipper ExternalClasses）
| 外部样式类名 | 说明 | 备注 |
| :--------- | :----------------- | :----- |
| l-class   | 最底层元素（组件总容器）外部样式类   |  ---   | 


## 组件事件（ImageClipper Events)

| 事件名称 | 说明 | 返回值	 | 备注 |
|:----|:----|:----|:----|:----|
| bind:linimageready	| 图片加载完成式触发	| - | - | 
| bind:linrotate	| 图片旋转时触发	| - | - | 
| bind:linsizechange	| 图片大小改变时触发	| - | - | 
| bind:linclip	| 图片裁剪完成后触发	| - | - | 

<RightMenu />


