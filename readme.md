# hover

一组CSS3动力悬停效果应用于链接，按钮，标志，SVG，精选图片等等。 轻松应用到自己的元素，修改或只是用于启发。 可用CSS，Sass和LESS。

[![explain](http://llever.com/explain.svg)](https://github.com/chinanf-boy/Source-Explain)
    
Explanation

> "version": "1.0.0" 让我们开始，漫长的`css`之旅吧

[github source](https://github.com/IanLunn/Hover)

~~[english](./README.en.md)~~

---

[hover 官方 demo](http://ianlunn.github.io/Hover/)

---

无可否认, css 每个属性的相关性, 都需要斟酌, 繁琐漫长

我们也总会找到, 一劳永逸的方式, css框架-比如最出名的[·bootstrap·](https://github.com/twbs/bootstrap)

似乎，每个公司都有自己的css框架，!那是一定的! 网站对应风格嘛, 

所以深层的道理是一样<开发者的事情❤️`me`>, 

看到的每个网站却也是不同的<那是设计师的事情💔>

---

## hover-explain-目录

- [css-框架的第一眼-bower.json](#css-入口)

- [复制-粘贴-一个效果](#复制-粘贴-一个效果)

- [从这里开始，我会分效果解释](#分隔-css-效果-解释)

---

## css-入口

bower.json

``` json
  "main": "css/hover.css",
```

## 复制-粘贴-一个效果

css 并不像 js 相互关联, 

也许一个效果, 只需要几行css代码, 所以复制/粘贴也是很重要的😊

比如`Grow 效果`-[codepen-例子](https://codepen.io/china-boy/pen/yvOgLV)

1. 下载Hover.css

2. 在中`css/hover.css`，找到`Grow CSS`（每个效果都使用上面的注释命名）：

``` css
/* Grow */
.hvr-grow {
    display: inline-block;
    vertical-align: middle;
    transform: translateZ(0);
    box-shadow: 0 0 1px rgba(0, 0, 0, 0);
    backface-visibility: hidden;
    -moz-osx-font-smoothing: grayscale;
    transition-duration: 0.3s;
    transition-property: transform;
}

.hvr-grow:hover,
.hvr-grow:focus,
.hvr-grow:active {
    transform: scale(1.1);
}
```

3. 复制此效果，然后将其粘贴到您自己的样式表中。

4. 在您想要显示效果的HTML文件中，将`class`添加`.hvr-grow`到您选择的元素。

``` html
<a href="#" class="hvr-grow">Add to Basket</a>
```

## 分隔-css-效果-解释

正如我上面所写, css-效果, 大多数情况下, 并不需要整个css文件

甚至说, 不会这个效果, 打开调试器, 找到css, 复制/粘贴就好了

还需要特地解释嘛, 

我也只能说, `知彼知己, 百战百胜`

> 接下来，我会根据-hover-给出的效果进行解释, 章节过长, 请选择感兴趣的🌟, 需要的❤️, 就好

反正, 转头就忘了, 这就是-css

---

[单个css-属性-解释](#css-属性-解释)

---

分-动画效果类型 < 前面详细, 后面只解释不同 >

- [ >> 2D-Transitions](#2d-transitions)

<details>

 <summary>更多 css 动画效果</summary>

- [-> 文件Background-Transitions](./background-transitions.md)

- [-> 文件Icons](./icons.md)

- [-> 文件Border-Transitions](./border-transitions.md)

- [-> 文件Shadow-and-Glow-Transitions](./shadow-and-glow-transitions.md)

- [-> 文件Speech-Bubbles](./speech-bubbles.md)

- [-> 文件Curl](./curl.md)

</details>

## 2D-Transitions

<details open>

 <summary>1. Grow </summary>

``` css
/* Grow */
.hvr-grow {
    display: inline-block; 
    /* 显示方式 > 内嵌区块 */
    vertical-align: middle;
    /* 反正就是对齐 */
    transform: translateZ(0);
    /*  */
    box-shadow: 0 0 1px rgba(0, 0, 0, 0);
    /* 区块阴影 */
    backface-visibility: hidden;
    /* 表示背面不可见 */
    -moz-osx-font-smoothing: grayscale;
    /* Firefox 用灰度抗锯齿渲染文本 */
    transition-duration: 0.3s;
    /*  动画时间 */
    transition-property: transform;
    /* css属性-transform 渐进变化 */
}

.hvr-grow:hover, /* 鼠标位于元素 */
.hvr-grow:focus,/* 当用户点击或触摸元素或通过键盘的 “tab” 键选择它时会被触发 */
.hvr-grow:active {/* 它代表的是用户按下按键和松开按键之间的时间 */
    transform: scale(1.1);
    /* 放大 */
}
```

> [css-属性解释](#css-属性-解释)

</details>

<details>

 <summary>2. Shrink</summary>

``` css
/* Shrink */
.hvr-shrink {
  display: inline-block;
  vertical-align: middle;
  -webkit-transform: perspective(1px) translateZ(0);
  /* -webkit- 各大内核的试验效果前缀 */
  /* perspective 属性指定了观察者与z=0平面的距离 */
  transform: perspective(1px) translateZ(0);
  box-shadow: 0 0 1px transparent;
  -webkit-transition-duration: 0.3s;
  transition-duration: 0.3s;
  -webkit-transition-property: transform;
  transition-property: transform;
}
.hvr-shrink:hover, .hvr-shrink:focus, .hvr-shrink:active {
  -webkit-transform: scale(0.9);
  transform: scale(0.9);
  /* 缩小 */
}
```

> [transform:perspective](#transform)

</details>

<details>

 <summary>3. Pulse</summary>

``` css
/* Pulse */
@-webkit-keyframes hvr-pulse {/*  动画效果名称-定义 */
  25% {  /* 时间 0% ～ 25% */
    -webkit-transform: scale(1.1);
    transform: scale(1.1);
    /*  先大 */
  }
  75% { /* 时间 25% ～ 75% */
    -webkit-transform: scale(0.9);
    transform: scale(0.9);
    /* 后小 */
  }
}
@keyframes hvr-pulse {
  25% {
    -webkit-transform: scale(1.1);
    transform: scale(1.1);
  }
  75% {
    -webkit-transform: scale(0.9);
    transform: scale(0.9);
  }
}
.hvr-pulse {
  display: inline-block;
  vertical-align: middle;
  -webkit-transform: perspective(1px) translateZ(0);
  transform: perspective(1px) translateZ(0);
  box-shadow: 0 0 1px transparent;
}
.hvr-pulse:hover, .hvr-pulse:focus, .hvr-pulse:active {
  /* 鼠标位于元素 */
/* 当用户点击或触摸元素或通过键盘的 “tab” 键选择它时会被触发 */
/* 它代表的是用户按下按键和松开按键之间的时间 */

  -webkit-animation-name: hvr-pulse;
  animation-name: hvr-pulse;
  /* 动画名字 */
  -webkit-animation-duration: 1s;
  animation-duration: 1s;
  -webkit-animation-timing-function: linear;
  animation-timing-function: linear;
  /* 动画-运动速率 */
  -webkit-animation-iteration-count: infinite;
  animation-iteration-count: infinite;
  /* infinite 无限循环播放动画. */

}
```
</details>

<details>

 <summary>4. Pulse-Grow</summary>

``` css
/* Pulse Grow */
@-webkit-keyframes hvr-pulse-grow {
  to {       /* 元素动画-最终形态 */
    -webkit-transform: scale(1.1);
    transform: scale(1.1);
  }
}
@keyframes hvr-pulse-grow {
  to {
    -webkit-transform: scale(1.1);
    transform: scale(1.1);
  }
}
.hvr-pulse-grow {
  display: inline-block;
  vertical-align: middle;
  -webkit-transform: perspective(1px) translateZ(0);
  transform: perspective(1px) translateZ(0);
  box-shadow: 0 0 1px transparent;
}
.hvr-pulse-grow:hover, .hvr-pulse-grow:focus, .hvr-pulse-grow:active {
  /* 鼠标位于元素 */
/* 当用户点击或触摸元素或通过键盘的 “tab” 键选择它时会被触发 */
/* 它代表的是用户按下按键和松开按键之间的时间 */

  -webkit-animation-name: hvr-pulse-grow;
  animation-name: hvr-pulse-grow;
  -webkit-animation-duration: 0.3s;
  animation-duration: 0.3s;
  -webkit-animation-timing-function: linear;
  animation-timing-function: linear;
  -webkit-animation-iteration-count: infinite;
  animation-iteration-count: infinite;
  /* infinite 无限循环播放动画. */
  -webkit-animation-direction: alternate;
  animation-direction: alternate;
  /* 动画交替反向运行 */
}
```
</details>

<details>

 <summary>5. Pulse-Shrink</summary>

``` css
/* Pulse Shrink */
@-webkit-keyframes hvr-pulse-shrink { 
  /* 动画名称-动作定义 */
  to {
    -webkit-transform: scale(0.9);
    transform: scale(0.9);
  }
}
@keyframes hvr-pulse-shrink {
  to {
    -webkit-transform: scale(0.9);
    transform: scale(0.9);
  }
}
.hvr-pulse-shrink {
  display: inline-block;
  vertical-align: middle;
  -webkit-transform: perspective(1px) translateZ(0);
  transform: perspective(1px) translateZ(0);
  box-shadow: 0 0 1px transparent;
}
.hvr-pulse-shrink:hover, .hvr-pulse-shrink:focus, .hvr-pulse-shrink:active {
  /* 鼠标位于元素 */
/* 当用户点击或触摸元素或通过键盘的 “tab” 键选择它时会被触发 */
/* 它代表的是用户按下按键和松开按键之间的时间 */

  -webkit-animation-name: hvr-pulse-shrink;
  animation-name: hvr-pulse-shrink;
  -webkit-animation-duration: 0.3s;
  animation-duration: 0.3s;
  -webkit-animation-timing-function: linear;
  animation-timing-function: linear;
  -webkit-animation-iteration-count: infinite;
  animation-iteration-count: infinite;
    /* infinite 无限循环播放动画. */
  -webkit-animation-direction: alternate;
  animation-direction: alternate;
   /* 动画交替反向运行 */
}
```

- [perspective](#transform)



</details>

<details>

 <summary>6. Push</summary>

``` css
/* Push */
@-webkit-keyframes hvr-push {
  /*  0%~50% 先小 */
  50% {
    -webkit-transform: scale(0.8);
    transform: scale(0.8);
  }
  /* 50%～100% 后大 */
  100% {
    -webkit-transform: scale(1);
    transform: scale(1);
  }
}
@keyframes hvr-push {
  50% {
    -webkit-transform: scale(0.8);
    transform: scale(0.8);
  }
  100% {
    -webkit-transform: scale(1);
    transform: scale(1);
  }
}
.hvr-push {
  display: inline-block;
  vertical-align: middle;
  -webkit-transform: perspective(1px) translateZ(0);
  transform: perspective(1px) translateZ(0);
  box-shadow: 0 0 1px transparent;
}
.hvr-push:hover, .hvr-push:focus, .hvr-push:active {
  /* 鼠标位于元素 */
  /* 当用户点击或触摸元素或通过键盘的 “tab” 键选择它时会被触发 */
  /* 它代表的是用户按下按键和松开按键之间的时间 */

  -webkit-animation-name: hvr-push;
  animation-name: hvr-push;
  -webkit-animation-duration: 0.3s;
  animation-duration: 0.3s;
  -webkit-animation-timing-function: linear;
  animation-timing-function: linear;
  -webkit-animation-iteration-count: 1;
  animation-iteration-count: 1;
  /*  运行一次 */
}
```
</details>

<details>

 <summary>7. Pop</summary>

``` css
/* Pop */
@-webkit-keyframes hvr-pop {
  /* 0~50% 大 */
  50% {
    -webkit-transform: scale(1.2);
    transform: scale(1.2);
  }
}
@keyframes hvr-pop {
  50% {
    -webkit-transform: scale(1.2);
    transform: scale(1.2);
  }
}
.hvr-pop {
  display: inline-block;
  vertical-align: middle;
  -webkit-transform: perspective(1px) translateZ(0);
  transform: perspective(1px) translateZ(0);
  box-shadow: 0 0 1px transparent;
}
.hvr-pop:hover, .hvr-pop:focus, .hvr-pop:active {
  -webkit-animation-name: hvr-pop;
  animation-name: hvr-pop;
  -webkit-animation-duration: 0.3s;
  animation-duration: 0.3s;
  -webkit-animation-timing-function: linear;
  animation-timing-function: linear;
  -webkit-animation-iteration-count: 1;
  animation-iteration-count: 1;
  /* 运行1次 */
}
```
</details>

<details>
 
<summary>8. Bounce In </summary>


``` css
/* Bounce In */
.hvr-bounce-in {
  display: inline-block;
  vertical-align: middle;
  -webkit-transform: perspective(1px) translateZ(0);
  transform: perspective(1px) translateZ(0);
  box-shadow: 0 0 1px transparent;
  -webkit-transition-duration: 0.5s;
  transition-duration: 0.5s;
}
.hvr-bounce-in:hover, .hvr-bounce-in:focus, .hvr-bounce-in:active {
  -webkit-transform: scale(1.2);
  transform: scale(1.2);
  /* 变大 */
  -webkit-transition-timing-function: cubic-bezier(0.47, 2.02, 0.31, -0.36);
  transition-timing-function: cubic-bezier(0.47, 2.02, 0.31, -0.36);
  /*  运动曲线 先快 中慢 后快 */
}
```
</details>

<details>

<summary>9. Bounce Out </summary>

``` css
/* Bounce Out */
.hvr-bounce-out {
  display: inline-block;
  vertical-align: middle;
  -webkit-transform: perspective(1px) translateZ(0);
  transform: perspective(1px) translateZ(0);
  box-shadow: 0 0 1px transparent;
  -webkit-transition-duration: 0.5s;
  transition-duration: 0.5s;
}
.hvr-bounce-out:hover, .hvr-bounce-out:focus, .hvr-bounce-out:active {
  -webkit-transform: scale(0.8);
  transform: scale(0.8);
  /* 变小 */
  -webkit-transition-timing-function: cubic-bezier(0.47, 2.02, 0.31, -0.36);
  transition-timing-function: cubic-bezier(0.47, 2.02, 0.31, -0.36);
  /*  运动曲线 先快 中慢 后快 */
  
}
```

</details>
---

### css-属性-解释

#### display

> CSS属性指定用于元素的呈现框的类型

#### vertical-align

> CSS 的属性 vertical-align 用来指定行内元素（inline）或表格单元格（table-cell）元素的垂直对齐方式。

> middle - 元素中垂线与父元素的基线加上小写x一半的高度值对齐。

#### transform

> CSS transform 属性允许你修改CSS视觉格式模型的坐标空间。使用它，元素可以被转换（translate）、旋转（rotate）、缩放（scale）、倾斜（skew）。 只应用-`display:*block*` 的元素

> [perspective >> 属性指定了观察者与z=0平面的距离](https://developer.mozilla.org/zh-CN/docs/Web/CSS/perspective)

#### box-shadow

> 定义元素-broder-边缘阴影

#### backface-visibility

>  属性指定当元素背面朝向观察者时是否可见

#### -moz-osx-font-smoothing

> Firefox 实现了名为 -moz-osx-font-smoothing 的相似属性。这个属性仅在 Mac OS X / macOS 下生效。

#### transition-duration

> 属性以秒或毫秒为单位指定过渡动画所需的时间。默认值为 0s ，表示不出现过渡动画

#### transition-property

> 指定哪个或哪些 CSS 属性用于过渡。只有指定的属性才会在过渡中发生动画，其它属性仍如通常那样瞬间变化。

#### animation-direction

>  CSS 属性指示动画是否反向播放

#### :hover

> CSS伪类适用于用户使用指示设备虚指一个元素（没有激活它）的情况

#### :focus

> 当用户点击或触摸元素或通过键盘的 “tab” 键选择它时会被触发

#### :active

> 它代表的是用户按下按键和松开按键之间的时间