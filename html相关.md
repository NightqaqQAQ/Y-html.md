## Font Awesome图标库
```html
<body>
    把图标做成字体  来使用 ,通过 font-size   color   属性 控制图标颜色和大小 -->
    1.下载 font-awesome
    2.引入css文件
    fa  和 fa前缀
    <div class="box">
        <i class="fa fa-camera-retro"></i>
        <i class="fa fa-arrow-down"></i>
    </div>
    标记语言
    <h2>标记语言</h2>

</body>
```
下好后引入**font-awesome.min.css**
- 你可以通过设置CSS前缀fa和图标的具体名称，来把Font Awesome 图标放在任意位置。Font Awesome 被设计为用于行内元素（我们喜欢用更简短的`<i>`标签，它的语义更加精准）。
- 例如: 默认图标如果您修改了图标容器的字体大小，图标大小会随之改变。同样也适用于颜色，阴影，阴影等其它任何CSS支持的效果上。
- font-awsome   只支持 675个图标
- 字体图标 不支持 多色图标
## iconfont
下载代码后引入
`<link rel="stylesheet" href="iconfont.css">`
然后从css中找到类名 `iconfont icon-gongpai`
```html
<body>
    <!-- font-awsome   只支持 675个图标 -->
    <!-- 字体图标 不支持 多色图标 -->
    <span class="iconfont icon-gongpai"></span>
</body>
```
> style选择时需要输入类名?