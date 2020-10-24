# **CSS**

## 1-SpinningAlbum

- section 里面包含 div
- 每个 div 绝对定位到 section 上面重叠起来，然后利用 3D 转换到空间里
- section 中要加 transform-style: preserve-3d; 来保证在 3d 运动的时候保留 3d 效果

## 4-2D-transform

- 分页按钮放大效果用 scale 而不是直接改宽度和高度。否则把后面的盒子挤跑了。

## 6-HotSpotMap

- 用阴影来扩张 instead of border
- 通过多类名来覆盖样式

animation 奔跑的熊 背景位置
transition 过渡
解构伪类选择器

# **JS**

## 1-CountDown

- 传进参数的标准写法:
  - 数字型 2019, 10, 01
  - 字符串型 '2019-10-1 8:8:8'
- 不能这样写，因为 date 存储的是那个时刻的时间，无论如何刷新页面都不会有变化
  ```javascript
  var date = new Date();
  setInterval(() => {
    div.innerHTML = `tody is ${date.toLocaleString()}`;
  }, 1000);
  ```
  应该这样写：
  ```javascript
  setInterval(() => {
    div.innerHTML = `tody is ${new Date().toLocaleString()}`;
  }, 1000);
  ```
- 只有 querySelector 有 innerHTML,用 getElementByTagName 就没有
