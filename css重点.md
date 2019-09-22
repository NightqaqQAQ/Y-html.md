# css常见单位
- px 像素单位，用于表示标签的宽和高，或者字体的大小。
百分比，通常用来表示长度或高度，相较于父类元素的百分比。
- em 基于当前字体的倍数
- 颜色
    - 预定义颜色：blue、yellow、pink、purple、red 等。
    - 十六进制：每两位表示一种颜色的深度，分别表示 red、green、blue，比如：`#ff00ff`。
    - rgb: `rgb(0,0,255) ==> `绿色。rgb 和十六进制是可以相互转换的。
    - rgba:`rgba(0,0,255,0.5)`。跟 rgb 一样，a 是透明度：0~1，0.5==> .5
    - transparent 透明色
# css常用属性
- wight/height  宽/高   px/%/em
- background-color  背景颜色  color
- color  字体颜色  color
- font-size  字体大小  px/em等
- text-align  文字对齐方式  center/left/right
- text-indent  首行缩进  px/em
- font-family  字体  微软雅黑Microsoft YaHei、黑体 SimHei、Arial 宋体等
- font-weight	 字体加粗  100-900.加粗 700-900/ bolder加粗 lighter变细  normal正常
- font-style	字体样式  italic 斜体 / normal 正常
- line-height	行高  单位： px /倍数 / 百分比 ;
    - 设置文字的行间距- 单行文字垂直居中 ：行高=父类盒子高度
- font	简易缩写  `font:italic(/斜体) bolder(/加粗) 20px/1.2(文字大小/行间距) 'Arial','Microsoft YaHei'(/字体样式)
- display: 修改元素的性质。
    - block：设置元素为块元素
    - inline：设置元素为行内元素
    - inline-block：设置元素为行内块元素
    - 转换的必要性：比如可以把a标签转换为块状元素，设置宽高，使用户可点击的区域增大，进而实现一个按钮的样式。
### 背景图片
- background-color  背景颜色  color
- background-image	背景图片  url(图片路径);
- background-repeat	平铺方式	repeat(平铺) 、 no-repeat(不平埔) 、 repeat-x(延水平方向平铺)) 、 repeat-y(延垂直方向平铺))
- background-position	图片位置	left、 right、 top、 bottom、 center(居中)
- background-attachment	背景滚动	scroll(不跟随网页滚动)、fixed(跟随网页滚动) (注意：基于 body 的定位）
- background	简写（顺序不能错）	background: green url(1.jpg) no-repeat center center fixed;

### 盒子模型
- CSS 处理网页时，它认为每个元素都包含在一个不可见的盒子里。包含内容区域、padding（内边距）、border（边框）、margin（盒子与盒子的距离）。

- 所有的页面的元素都可以看成是一个盒子，占据一定的页面空间。



#### padding
- padding:10px 20px 30px 40px; 这样会设置元素的上、右、下、左四个方向的内边距。
- padding:10px 20px 30px; 分别指定上、左右、下四个方向的内边距。
- padding:10px 20px; 分别指定上下、左右四个方向的内边距。
- padding:10px; 同时指定上左右下四个方向的内边距。
同时在 css 中还提供了 padding-top、padding-left、padding-right、padding-bottom 分别用来指定四个方向的内边距。
- 不管设置哪个属性  都会改变元素的大小
#### margin
- 设置方法和padding类似，同样也提供了四个方向的 margin-top/margin-right/margin-bottom/margin-left。
- margin: xxx auto;可以使块状元素水平居中。
- 嵌套崩塌：两个盒子发生嵌套的时候，给子类设置 margin 会给父类造成一种崩塌现象，子类元素的 margin-top 没有效果，而是直接作用到父类元素。
解决方案：
    - 1. 父类 overflow: hidden;
    - 2. 父类 设置极小的 padding 或者 border；
- margin重叠： 如果垂直方向上两个块状元素同时设置了 margin-bottom 和 margin-top，那么这两个值将会发生重叠，不会累加，哪个值大用哪个。
- margin-top/margin-bottom 对于行内元素无效。
- 不管设置哪个属性  都会改变元素的大小
#### border
- 可以在元素周围创建边框，边框是元素可见框的最外部。
- border:1px solid red; 分别指定了边框的宽度、颜色和样式，是一种缩写：border-width border-style border-color。
- border-style: none (默认) / dashed(虚线) / dotted（点） / solid(实线) / double(双实线)。
- 可以单独设置某一条边框：border-right: 20px solid blue;
- 不管设置哪个属性  都会改变元素的大小
#### 显示和隐藏
- display:none; 隐藏元素，不再在文档中占据位置。
显示：可以将 display 设置为其他属性值，不为 none 即可。
    - 隐藏后不可点击 设置hover时设置其父类
- visibility:hidden; 隐藏元素，隐藏后其在文档中所占的位置会依然保持，不会被其他元素覆盖。visibility: visible显示
    - 隐藏后不可点击 设置hover时设置其父类
#### overflow
- overflow 指定标签里面的内容超出了样式的宽度和高度时如何处理。
    - visible：默认值
    - scroll：添加滚动条
    - auto：根据需要添加滚动条
    - hidden：隐藏超出盒子的内容

## 文档流
- 块状元素独占一行
- 行内元素可以同一行显示，自左向右，如果不够会自动换行
- 自上而下的展示
- 脱离文档流：浮动和定位
- 当浮动后 剩余的内容自适应
### 浮动
- 浮动指的是使元素脱离原来的文本流，在父元素中浮动起来。

- 浮动使用 float 属性。
- 可选值：
    - none：不浮动
    - left：向左浮动
    - right：向右浮动
##### 浮动的表现形式
- 当一个元素浮动以后，其下方的元素会上移。元素中的内容将会围绕在元素的周围。
- 浮动会使元素完全脱离文本流，也就是不再在文档中在占用位置。
- 元素设置浮动以后，会一直向上漂浮直到遇到父元素的边界/其他浮动元素/已经占位的兄第元素。
- 元素浮动以后即完全脱离文档流，这时不会再影响父元素的高度。也就是浮动元素不会撑开父元素。
- 浮动元素默认会变为块元素，即使设置 display:inline 以后其依然是个块元素。
- 块级元素和行内元素都可以浮动，当一个行内元素浮动以后将会自动变为一个块级元素。
- 当一个块级元素浮动以后，宽度会默认被内容撑开，所以当漂浮一个块级元素时我们都会为其指定一个宽度。
##### 浮动的影响
如果子类元素设置了浮动，而父类元素没有设置高度，或者高度比子类元素小，那么子类元素脱离了文档流，就无法把父类盒子撑开。那么整个文档的结构将受到破坏。

**清除浮动的影响：**
- 严格计算父类盒子高度
    - clear: left/right/both 不允许当前元素的 left/right/both 有浮动元素。
    - 在浮动元素的最后面追加一个空的 div,设置 clear:both 即可清除浮动的影响。
    - 因为浮动会对文档流造成影响，所以能用流式布局就不要使用浮动。
- 补充：
    - 1.display：inline-block 标签的换行符会被显示为空格。
    - 2.float:right 会改变标签的前后顺序。


## 定位
- 通过 position 属性可以实现元素的定位。元素定位之后，需要通过设置 left/right 和 top/bottom 值对元素定位。

- position 属性可以把一个元素放置到网页中的任何位置。

- 可选值：

    - static（默认  没有定位）
    - relative(相对定位)
    - absolute(绝对定位)
    - fixed(固定定位)
    - sticky(粘性定位)
## relative 相对定位
相对元素本身的位置定位。

- 每个元素在页面的文档流中都有一个自然位置。相对于这个位置对元素进行移动就称为相对定位。周围的元素完全不受此影响。
- 当开启了相对定位以后，可以使用 top、right、bottom、left 四个属性对元素进行定位。
如果不设置元素的偏移量，元素位置不会发生改变。
相对定位不会使元素脱离文本流。元素在文本流中的位置不会改变。
相对定位不会改变元素原来的特性。
相对定位会使元素的层级提升，使元素可以覆盖文本流中的元素。

## absolute 绝对定位
指使元素相对于视口或离他最近的祖先定位元素进行定位。

- 当开启了绝对定位以后，可以使用 top、right、bottom、left 四个属性对元素进行定位。
- 绝对定位会使元素完全脱离文本流。
- 绝对定位的块元素的宽度会被其内容撑开。
- 绝对定位会使行内元素变成块元素。
- 一般使用绝对定位时会同时为其父元素指定一个相对定位，以确保元素可以相对于父元素进行定位。

## fixed 固定定位
元素会被锁定在屏幕的某个位置上，当访问者滚动网页时，固定元素会在屏幕上保持不动。 (相对于视口定位)

- 固定定位不占据原来的位置，会脱离文档流。
- 给元素设置固定定位之后，元素位置从浏览器左上角出发。 - 可以将行内元素转换块元素。

## sticky 粘性定位
粘性定位可以被认为是相对定位和固定定位的混合。元素在跨越特定阈值前为相对定位，之后为固定定位。

`#one {
	position: sticky;
	top: 10px;
}`
在网页滚动到元素 top 距离小于 10px 之前，元素为相对定位。之后，元素将固定在与顶部距离 10px 的位置，直到 网页回滚到阈值以下。

## z-index
- 当元素开启定位以后就可以设置 z-index 这个属性。默认是 0。
- z-index 可以指定一个整数作为参数，值越大元素显示的优先级越高，也就是 z-index 值较大的元素会显示在网页的最上层。

# css书写位置
- 行内样式 `<p style="color: red; font-size: 24px;">`这是一个p标签`</p>`
- 内部样式 `<style>p{color: red;font-size: 24px;}</style>`
- 外部引入 `<link rel="stylesheet" href="style.css">`
- 区别
    - 行内样式：严重耦合，用的很少。
    - 内部样式：测试使用，当前页面的样式只能当前页面使用。
    - 外部样式：上线使用，多个页面可以复用样式。
# CSS 选择器
- 简单选择器
    - 标签选择器 p{}
    - id 选择器 #p{}
    - class 选择器 .p{}
- 复杂选择器
    - 交集选择器
        - p.p1{}选中同时拥有这两个名字的元素
    - 并集选择器
        - p,
        p1{}同时选中这两个元素
    - 后代选择器
        - p .p1{}中间有空格 选中p标签里边所有的.p1元素
    - 通配符
        - *{}选中所有元素
    - 子类选择器
        - p>.p1{}选中p标签的子类p1元素
    - 相邻兄第选择器
        - p+p1{}选中p标签的下一个兄弟元素 只能选一个
    - 大哥选择器
        - p~.p1{}选中p标签后面所有兄弟元素
# CSS 继承性
[css 中可以和不可以继承的属性总结](https://www.cnblogs.com/thislbq/p/5882105.html)
# CSS 层叠性
样式冲突，必然只有一个样式生效。

# CSS 权重问题
- 行内样式 > id 选择器 > class 选择器 >标签选择器
- 复杂选择器权重计算
    - 行内样式 1000
    - id 选择器 100
    - class 选择器 10
    - 标签选择器 1
    - 通配符/继承属性 0
- 如果两个选择器是一样的，遵循就近原则。
- 如果写了相同的选择器，希望某个选择器权重更高，添加 class 类名，使用交集选择器即可。
## 规避脱标流
- 经验： 一般布局采用标准流，如果标准流布局实现不了用浮动。定位一般用于解决小范围的某个标签的位置。

- 能用标准流（没有脱标）解决就不用浮动
- 解决不了就考虑有浮动（页面布局类型，“不完全脱标”）
- f浮动解决不了用定位（小图标，完全脱标，不影响内容）

# transfrom
- transform: translateX(-50%) translateY(-50%);
    - 简易写法 transform: translate(-50%, -50%);
    - 向左移动自身的50% 向上移自身的50%
    - 坐标系X轴右是正
    - 坐标系Y轴下是正
- transform: rotate(135deg);
    - 旋转自身平面135度 deg度
# transition
- transition-property	规定设置过渡效果的 CSS 属性的名称。
- transition-duration	规定完成过渡效果需要多少秒或毫秒。
- transition-timing-function	规定速度效果的速度曲线。
- transition-delay	定义过渡效果何时开始。
- 简写transition: all(所有属性) ease 3s(减缓时间);