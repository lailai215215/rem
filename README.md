# rem
移动端通过控制 viewport 和根字体，使用 rem 进行屏幕适配

### 一、使用方法

```
<!DOCTYPE html>
<html>
	<head>
		<script src="rem-dpr.min.js" type="text/javascript" charset="utf-8"></script>
		//请勿自行添加 viewport ，js 中自动设置
	</head>
	<body>
	</body>
</html>

```
### 二、文件说明

## rem-dpr
> 1. 检测设备像素比 window.devicePixelRatio
> 2. 根据像素比设置 viewport 缩放实现高清
> 3. 设定基准 dpr 为 2 下根字体大小 100px

主要设备统计：

设备名称  | dpr | viewport 缩放 | viewport 屏宽 | 根字体 | 高清 |
---|---|---|---|---|---
iPhone 4 | 2 | 0.5 | 640 px | 100 px | 是 |
iPhone 5 | 2 | 0.5 | 640 px | 100 px | 是 |
iPhone 6 | 2 | 0.5 | 750 px | 100 px | 是 |
iPhone 6 Plus| 3 | 1/3 | 1242 px | 150 px | 是 |

使用建议：
- 【推荐】不同设备搭配@media使用效果好，特别是同时pad大屏，只需设置媒体值查询，即可实现良好排版。但无法保持不同的设备上完全等比例实现 psd 图效果。

## rem-dpr-w
> 1. 检测设备像素比 window.devicePixelRatio
> 2. 根据像素比设置 viewport 缩放实现高清
> 3. 设置基准 640px 视窗宽度下，根字体大小为 100px

主要设备统计：

设备名称  | dpr | viewport 缩放 | viewport 屏宽 | 根字体 | 高清 |
---|---|---|---|---|---
iPhone 4 | 2 | 0.5 | 640 px | 100 px | 是 |
iPhone 5 | 2 | 0.5 | 640 px | 100 px | 是 |
iPhone 6 | 2 | 0.5 | 750 px | 117.188 px | 是 |
iPhone 6 Plus| 3 | 1/3 | 1242 px | 194.063 px | 是 |

使用建议：
- 如果要保持页面在不同设备下完全等比例缩放元件，赶快来使用吧！但纵向无法保持在宽高比不同的设备上等完全等比例实现 psd 图效果

## rem-dpr-h
> 1. 检测设备像素比 window.devicePixelRatio
> 2. 根据像素比设置 viewport 缩放实现高清
> 3. 设置基准 640px 视窗高度下，根字体大小为 100px

主要设备统计：

设备名称  | dpr | viewport 缩放 | viewport 屏宽 | 根字体 | 高清 |
---|---|---|---|---|---
iPhone 4 | 2 | 0.5 | 640 px | 150 px | 是 |
iPhone 5 | 2 | 0.5 | 640 px | 177.5 px | 是 |
iPhone 6 | 2 | 0.5 | 750 px | 208.438 px | 是 |
iPhone 6 Plus| 3 | 1/3 | 1242 px | 345 px | 是 |

使用建议：
- 如果要保持页面在不同设备下尽可能与psd图保持一致，等比例缩放，赶快来使用吧！但pad上也会等比例，很丑哦
