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

---

### 2D-Transitions



---

### Background-Transitions

---

### Icons

---

### Border-Transitions

---

### Shadow-and-Glow-Transitions


---

### Speech-Bubbles


---

### Curl
