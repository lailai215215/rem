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
debug 文件设置 window.onresize 重新计算，便于调试

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
- 可以实现高清，体验更好，推荐使用！但无法保持不同的设备上完全等比例实现 psd 图效果。

## rem-w
> 1. 设置 viewport 缩放为 1.0
> 2. 检测视窗宽度 clientWidth
> 3. 设置基准 640px 视窗宽度下，根字体大小为 100px

主要设备统计：

设备名称  | viewport 屏宽 | 根字体 | 高清 |
---|---|---|---|---|---
iPhone 4 | 320 px | 50 px | 否 |
iPhone 5 | 320 px | 50 px | 否 |
iPhone 6 | 375 px | 58.5938 px | 否 |
iPhone 6 Plus| 414 px | 64.6875 px | 否 |

使用建议：
- 如果要保持页面在不同设备下完全等比例缩放元件的情况下，赶快来使用吧！但纵向无法保持在宽高比不同的设备上等完全等比例实现 psd 图效果，并且不支持高清哦

## rem-h
> 1. 设置 viewport 缩放为 1.0
> 2. 检测视窗宽度 clientHeight
> 3. 设置基准 640px 视窗高度下，根字体大小为 100px

主要设备统计：

设备名称  | viewport 高宽 | 根字体 | 高清 |
---|---|---|---|---|---
iPhone 4 | 480 px | 75 px | 否 |
iPhone 5 | 568 px | 88.75 px | 否 |
iPhone 6 | 667 px | 104.219 px | 否 |
iPhone 6 Plus| 736 px | 115 px | 否 |

使用建议：
- 如果要保持页面在不同设备满屏下等比例缩放，并且优先考虑页面纵向在宽高比不同的设备中能够实现等比例缩放的情况下，赶快来使用吧！但不支持高清哦
