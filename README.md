# learn-canvas
learn canvas, just some demo

### 目录
+ index.html -- canvas 基础
+ particle.html -- 实现随机粒子

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

### 绘制图像的步骤

+ 开始一个路径 beginPath()
+ 绘制路径
+ 关闭路径 closePath()
+ 设置填充颜色或描边颜色
+ 填充颜色或描边

### arc() 绘制弧/曲线

```
context.arc(x, y, r, sAngle, eAngle, counterclockwise);
```

+ x: 圆心的 x 坐标
+ y：圆心的 y 坐标
+ r：半径
+ sAngle：起始角，以弧度计（弧的圆形的三点钟位置是 0 度）
+ eAngle：结束角
+ counterclockwise：可选，true 逆时针绘制；false 顺时针绘制

### 给直线添加样式

| 样式 | 描述 |
| ---- | ---- |
| lineCap | 设置或返回线条的结束端点样式 |
| lineJoin | 设置或返回两条线相交时，所创建的拐角类型 |
| lineWidth | 设置或返回当前的线条宽度 |
| miterLimit | 设置或返回最大衔接长度 | 

### 绘制矩形

+ fillRect(x, y, width, height)：绘制一个实心矩形
+ fillStyle


+ strokeRect(x, y, width, height)：绘制一个空心矩形
+ strokeStyle

### 路径属性

| 属性 | 描述 |
| ---- | ---- |
| fillStyle | 设置或返回用于填充绘画的颜色、渐变或模式 |
| strokeStyle | 设置或返回用于笔触的颜色、渐变或模式 |
| shadowColor | 设置或返回用于阴影的颜色 |
| shadowBlur | 设置或返回用于阴影的模糊级别 |
| shadowOffsetX | 设置或返回阴影距形状的水平距离 |
| shadowOffsetY | 设置或返回阴影距形状的垂直距离 | 

### 设置渐变

| 方法 | 描述 |
| ---- | ---- |
| createLinearGradient() | 创建线性渐变（用在画布内容上）|
| createPattern() | 在指定的方向上重复指定的元素 |
| createRadialGradient() | 创建放射状/环形的渐变（用在画布内容上）|
| addColorStop() | 规定渐变对象中的颜色和停止位置 |

+ context.createLinearGradient(x0, y0, x1, y1)
    - x0：开始渐变的 x 坐标
    - y0：开始渐变的 y 坐标
    - x1：结束渐变的 x 坐标
    - y1：结束渐变的 y 坐标


### 图形转换

| 方法 | 描述 |
| ---- | ---- |
| scale() | 缩放当前绘图至更大或更小 |
| rotate() | 旋转当前绘图 |
| translate() | 重新映射画布上的 (0,0) 位置 |
| transform() | 替换绘图的当前转换矩阵 |
| setTransform() | 将当前转换重置为单位矩阵，然后运行 transform() | 


