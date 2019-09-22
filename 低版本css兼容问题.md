# CSS 兼容处理
在不支持 HTML5 新标签的浏览器里，会将这些新的标签解析成行内元素（inline）对待，所以我们只需要将其转换成块元素（block）即可使用，但是在 IE9 版本以下，并不能正常解析这些新标签，但是却可以识别通过 document.createElement('tagName') 创建的自定义标签，于是我们的解决方案就是将 HTML5 的新标签全部通过 document.createElement('tagName') 来创建一遍，这样 IE 低版本也能正常解析 HTML5 新标签了，在实际开发中我们更多采用的是通过检测 IE 浏览器的版本来加载三方的一个 JS 库（html5shiv.min.js）来解决兼容问题。

`<!--[if gte IE 7]> <link rel="stylesheet" href="ie10.css"> <![endif]-->`
`<!--[if lte IE 8]> <script src="html5shiv.min.js"></script> <![endif]-->`
- 注意: 在非IE浏览器中是看不到效果的

    - lte：就是Less than or equal to的简写，也就是小于或等于的意思。
    - lt ：就是Less than的简写，也就是小于的意思。
    - gte：就是Greater than or equal to的简写，也就是大于或等于的意思。
    - gt ：就是Greater than的简写，也就是大于的意思。
    - !： 就是不等于的意思，跟javascript里的不等于判断符相同