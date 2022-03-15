## CanvasGradient 对象

`CanvasGradient` 用于描述一个渐变，可以是线性渐变或者放射渐变

它没有任何属性，也没有构造函数，只有一个方法 `addColorStop()` 用于增减一个渐变点

## CanvasGradient.addColorStop()

`addColorStop` 用于添加一个由偏移 ( offset )和颜色( color )定义的色标 ( color stops) 到渐变中

如果偏移值不在 0 到 1 之间，将抛出 `INDEX_SIZE_ERR`错误

如果颜色值不能被解析为有效的 CSS 颜色值 ，将抛出 `SYNTAX_ERR` 错误

### 语法

```
void gradient.addColorStop(offset, color);
```

| 参数   | 说明            |
| ------ | --------------- |
| offset | 0 到 1 之间的值 |
| color  | CSS颜色值       |

## 创建渐变的方法

Canvas 提供了两个方法用于创建渐变对象

| 方法                                         | 说明     |
| -------------------------------------------- | -------- |
| createLinearGradient(x1, y1, x2, y2)         | 线性渐变 |
| createRadialGradient(x1, y1, r1, x2, y2, r2) | 放射渐变 |

有了渐变对象后，我们就可以把它赋值给 `strokeStyle` 或者 `fillStyle` 那么新绘制的图形或者路径就会有渐变效果

## Canvas 线性渐变 ( LinearGradient )

线性渐变 ( LinearGradient ) 就是从一个颜色值直线性的渐变到另一个颜色值

![img](https://www.twle.cn/static/i/canvas/canvas_gradient_line_1.png)

Canvas 使用 `createLinearGradient()` 方法创建一个线性渐变

### createLinearGradient()

`createLinearGradient()` 创建一个沿参数坐标指定的直线的渐变，并返回一个渐变 CanvasGradient 对象

#### 语法

```
CanvasGradient ctx.createLinearGradient(x0, y0, x1, y1);
```

| 参数 | 说明            |
| ---- | --------------- |
| x0   | 起点的 x 轴坐标 |
| y0   | 起点的 y 轴坐标 |
| x1   | 终点的 x 轴坐标 |
| y1   | 终点的 y 轴坐标 |

### 线性渐变的使用方法

1. 使用 `createLinearGradient()` 方法创建一个指定了开始和结束点的 CanvasGradient 对象
2. 创建成功后，可以使用 `CanvasGradient.addColorStop()`方法添加起始色标
3. 然后把渐变对象赋值给 `strokeStyle` 或者 `fillStyle` 属性

## Canvas 放射渐变 ( RadialGradient )

放射渐变 ( RadialGradient ) 就是从一个颜色值以一个点为中心向四周扩散到另一个颜色值

![img](https://www.twle.cn/static/i/canvas/canvas_gradient_radial_1.png)

Canvas 使用 `createRadialGradient()` 方法创建一个线性渐变

### createRadialGradient()

`createRadialGradient()` 根据参数确定两个圆的坐标，绘制放射性渐变，并返回一个渐变 CanvasGradient 对象

#### 语法

```
CanvasGradient ctx.createRadialGradient(x0, y0, r0, x1, y1, r1);
```

| 参数 | 说明                |
| ---- | ------------------- |
| x0   | 开始圆形的 x 轴坐标 |
| y0   | 开始圆形的 y 轴坐标 |
| r0   | 开始圆形的半径      |
| x1   | 结束圆形的 x 轴坐标 |
| y1   | 结束圆形的 y 轴坐标 |
| r1   | 结束圆形的半径      |

### 放射渐变的使用方法

1. 使用 `createRadialGradient()` 方法创建一个指定了开始和结束点的 CanvasGradient 对象
2. 创建成功后，可以使用 `CanvasGradient.addColorStop()`方法添加起始色标
3. 然后把渐变对象赋值给 `strokeStyle` 或者 `fillStyle` 属性