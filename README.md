# learn-canvas
learn canvas, just some demo

### 创建画布

用 HTML 或 JS 设置画布宽高，不要用 CSS，因为会缩放

### 获取 Canvas 对象

```
var canvas = document.getElementById('canvas');
var context = canvas.getContext(contextType);
```

contextType: 
+ 2d
+ webgl
+ webgl2

### 绘制路径

| 方法 | 描述 |
| ---- | ---- |
| fill() | 填充路径 |
| stroke() | 描边 |
| arc() | 创建圆弧 |
| rect() | 创建矩形 |
| fillRect() | 绘制矩形路径区域 |
| strokenRect() | 绘制矩形路径描边 |
| clearRect() | 在给定的矩形内清除指定的像素 |
| arcTo() | 创建两切线之间的弧/曲线 |
| beginPath() | 起始一条路径，或重置当前路径 |
| moveTo() | 把路径移动到画布中的指定点，不创建线条 |
| lineTo() | 添加一个新点，然后在画布中创建从该点到最后指定点的线条 |
| closePath() | 创建从当前点回到起始点的路径 |
| clip() | 从原始画布剪切任意形状和尺寸的区域 | 
| quadraticCurveTo() | 创建二次方贝塞尔曲线 |
| bezierCurveTo() | 创建三次方贝塞尔曲线 |
| isPointInPath() | 如果指定的点位于当前路径中，则返回 true，否则返回 false |
