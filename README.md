# Slider

此插件依赖 [zepto.js](http://zeptojs.com/)

> 开启延迟加载建议设置src属性为小图片，推荐使用base64，避免发起HTTP请求

## Options

`index` {Number} 初始索引位置，默认： `0`

`duration` {Number} 动画过渡时间， 默认：`400ms`

`autoplay` {Boolean} 是否自动滑动，默认：`false`

`interval` {Number} 自动滑动间隔时间，默认：`3000ms`

`lazyload` {Boolean} 是否开启延迟加载，默认：`false`

`attribute` {String} 设置图像真实的url存储在哪个属性中，当开启延迟加载时有效，默认：`data-url`

`vertical` {Boolean} 是否启用垂直方向滑动，默认：`false`

## Methods

### destroy  
销毁当前实例  

```js
$('#slider').slider('option', 'destroy');
```
### slideTo  
设置slider的索引值  

```js
$('#slider').slider('option', 'slideTo', 1);
```
### getIndex  
获取slider当前的索引值  

```js
$('#slider').slider('option', 'getIndex');
```
### refresh  
刷新slider  

```js
$('#slider').slider('option', 'refresh');
```

## Examples

```html
<div id="slider">
  <div class="slider-item">
    <img src="1.jpg" alt="1.jpg">
  </div>
  <div class="slider-item">
    <img src="2.jpg" alt="2.jpg">
  </div>
  <div class="slider-item">
    <img src="3.jpg" alt="3.jpg">
  </div>
</div>
```

```css
body {
  margin: 0;
}
.container {
  position: relative;
  width: 100%;
  overflow: hidden;
  height: 12.5rem;
}
.slider-item > img {
  max-width: 100%;
}
```

```js
(function($){
  $('#slider').slider();
})(Zepto);

```

## License

MIT
