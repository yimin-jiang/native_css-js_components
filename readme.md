# **CSS**

## 1-SpinningAlbum

- section 里面包含 div
- 每个 div 绝对定位到 section 上面重叠起来，然后利用 3D 转换到空间里
- section 中要加 transform-style: preserve-3d; 来保证在 3d 运动的时候保留 3d 效果

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
