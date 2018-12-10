### seiper
---
https://github.com/nolimits4web/Swiper

```
npm install --global gulp
npm install
npm run build:dev
npm run build:prod
```

```js
var mySwiper = new Swiper('.swiper-container', {
  spped: 400,
  spaceBetween: 100
});

var mySwiper = document.querySelector('.swiper-container').swiper
mySwiper.slideNext();

var mySwiper = new Swiper('.swiper-container', {
  on: {
    init: function(){
      console.log('swiper initialized');
    },
  },
});

var mySwiper = new Swiper('.swiper-container', {
});
mySwiper.on('slideChange', function(){
  console.log('slied changed');
});

var swiper = new Swiper('.swiper-container', {
  preloadImages: false,
  lazy: true
});

```

```
```


