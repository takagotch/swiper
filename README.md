### swiper
---
https://github.com/nolimits4web/Swiper

```sh
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

```js
import { Swiper, Navigation, Pagination, Scrollbar } from 'swiper/dist/js/swiper.esm.js';
Swiper.use();

var swiper = new Swiper('.swiper-container', {
  speed: 500,
  navigation: {
    nextEl: '.swiper-button-next',
    prevEl: '.swiper-button-prev',
  },
});

//vue.js
import Swiper form 'swiper/dist/js/swiper.esm.bundle';
export default {
  data(){
    return {
      slides: (function(){
        var slides = [];
        for(var i = 0; i < 600; i += 1){
          slides.push('Slide ' + (i + 1));
        }
        return slides;
      }()),
      virtualData: {
        slides: [],
      },
    },
    mounted(){
      const self = this;
      const swiper = new Swiper('.swiper-container', {
        virtual: {
          slides: self.slides,
          renderExternal(data){
            self.vitualData = data;
          },
        },
      });
    },
  }
};

//react.js
import React from 'react';
import Swiper from 'swiper/dist/js/swiper.esm.bundle';

export default class extends React.Component {
  constructor(){
    this.state = {
      slides: (function(){
        var slides = [];
        for(var i = 0; i < 600; i += 1){
          slides.push('Slide ' + (i + 1));
        }
        return slides;
      }()),
      virtualData: {
        slides: [],
      },
    }
  }
  componentDidMount(){
    const self = this;
    const swiper = new Swiper('.swiper-container', {
      virtual: {
        slides: self.state.slides,
        renderExternal(data){
          self.setState({
            virtualData: data,
          });
        }
      },
    });
  }
  render(){
    { /* ... */ }
    <div className="swiper-container">
      <div className="swiper-wrapper">
        { /* */ }
        {this.state.virtualData.slides.map((slide, index) => (
          <div className="swiper-slide"
            key={index}
            style={{left: `${virtualData.offset}px`}}
          >{slide}</div>
        ))}
      </div>
    </div>
    { /* ... */ }
  }
}

var swiper = new Swiper('.swiper-container', {
  hashNavigation: true
})

module.exports = {
  components: [
    'virtual',
    'keyboard',
  ],
  target: 'universal',
  themeColor: '#007aff',
  colors: {
    white: '#ffffff',
    black: '#000000',
  },
};
```


