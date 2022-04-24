# Canvas 纹理 ( Pattern )

## createPattern()

`ctx.createPattern()` 方法用于创建一个纹理，可以使用图像或者另一个 Canvas

### 语法

```
CanvasPattern ctx.createPattern(image, repetition);
```

#### 参数说明

1. **image**

   作为重复图像源的 CanvasImageSource 对象。可以是下列之一

   ```
   HTMLImageElement (<img>),
   HTMLVideoElement (<video>),
   HTMLCanvasElement (<canvas>),
   CanvasRenderingContext2D,
   ImageBitmap,
   ImageData,
   Blob
   ```

2. **repetition**

   指定如何重复图像。允许的值有

   | 值        | 说明                   |
   | --------- | ---------------------- |
   | repeat    | 水平和垂直都重复，默认 |
   | repeat-x  | 水平重复               |
   | repeat-y  | 垂直重复               |
   | no-repeat | 不重复                 |

   如果为空字符串 ('') 或 null (但不是 undefined)，那么将使用 `repeat`

## 纹理的使用方法

1. 使用 `createPattern()` 方法创建一个纹理对象
2. 然后把渐变对象赋值给 `fillStyle` 属性