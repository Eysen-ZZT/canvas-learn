## strokeRect

渲染上下文 ( ctx ) 提供了 `strokeRect()` 方法用来绘制一个矩形

要绘制一个矩形，有两种办法

1. 确定起始坐标 `(x1,y1)` 和矩形斜角坐标 `(x2,y2)`，然后确定剩下的坐标，最后用直线连起来
2. 取定起始坐标 `(x1,y1)` 和长宽 `(width,height)`,然后画出来即可

**语法**

```js
strokeRect(x, y, width, height)
```

| 参数   | 说明          |
| ------ | ------------- |
| x      | 起始点 x 坐标 |
| y      | 起始点 y 坐标 |
| width  | 矩形长度      |
| height | 矩形高度      |

## strokeStyle

`ctx.strokeStyle` 属性用于设置画笔(绘制图形)颜色或者样式

默认值是黑色 `#000` (black)

> `strokeStyle` 一旦设置就会成为接下来的默认画笔，除非再次调用设置为其它的值

**语法**

```js
ctx.strokeStyle = color;
ctx.strokeStyle = gradient;
ctx.strokeStyle = pattern;
```

| 值       | 说明                                                         |
| :------- | :----------------------------------------------------------- |
| color    | 一个字符串颜色值，可以是任意的 CSS 颜色值，比如 `red` 、`#000` 等 |
| gradient | 一个渐变，是一个 `CanvasGradient` 对象 ( 线性渐变或放射性渐变)，我们后面会讲 |
| pattern  | 一个绘画对象，是一个 CanvasPattern 对象 ( 可重复的图片)，可以是一张图片，或者另一个画布 |

## fillRect

`fillRect()` 方法和 `strokeRect()` 方法一样，不同的是它会使用特定的颜色(默认为黑色)来填充矩形

**语法**

```js
strokeRect(x, y, width, height)
```

| 参数   | 说明          |
| ------ | ------------- |
| x      | 起始点 x 坐标 |
| y      | 起始点 y 坐标 |
| width  | 矩形长度      |
| height | 矩形高度      |

## fillStyle

`ctx.fillStyle` 属性用于设置填充(绘制图形)颜色或者样式

默认值是黑色 `#000` (black)

语法和strokeRect 基本一致