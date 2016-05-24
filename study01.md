###定位 position

##position 无继承性
static:无特殊定位，对象遵循正常的文档流，top等值无效

##z-index 无继承性
值：auto，继承父对象的定位
规则：并级的对象，此属性参数值越大，则被层叠在最上面。
      如两个对象的此属性具有同样的值，那么将依据它们在HTML文档中流的顺序层叠，写在后面的将会覆盖前面的。
      必须定义position属性值为absolute、relative或fixed，此取值方可生效。
      对应的脚本特性为zIndex。

###布局 layout 无继承性
#display 无继承性
值：table-cell,指定对象为块元素的表格，可以使用表格的特殊样式
兼容性：IE7及更早浏览器只支持none | inline | block | inline-block | list-item参数值。

#clear 无继承性
left:清除之前元素的左浮动影响，就相当于之前元素没有设置浮动
right:清除之前元素的右浮动影响，就相当于之前元素没有设置浮动
both:清除之前元素的左和右浮动影响，就相当于之前元素没有设置浮动

#visibility 无继承性
该属性与display不同，此属性为隐藏的对象保留其物理空间
值：collapse，对表格对象隐藏边框，对其他对象相当于hidden

#overflow 无继承性
值：visible 所有内容可视
    hidden:超出内容隐藏
    scroll：超出内容可以通过滚动条查看
    auto:需要时自动添加滚动条
类似的：overflow-x overflow-y

###弹性盒模型  CSS3

#box-orient 无继承性  
值：horizontal:设置弹性盒模型对象的子元素水平排列
    vertical：设置弹性盒模型对象的子元素为纵向排列



###边框 Border 

#border-image 无继承性 CSS3
border-image：border-image-source || border-image-slice? [ / border-image-width ?][ / border-image-outset? ] ] || [border-image-repeat]
border-image-source:图片地址
border-image-slice：图片做成边框的样式
border-image-repeat：图片的重复方式

#border-top-left-radius ...

#border-reflect  无继承性 CSS3 设置图片镜像/倒影
    box-reflect：none | <direction> <offset>? <mask-box-image>?
         <direction> = above | below | left | right
         <offset> = <length> | <percentage>
         <mask-box-image> = none | <url> | <linear-gradient> | <radial-gradient> | <repeating-linear-gradient> | <repeating-radial-gradient>
    默认值：none


###背景 background


#backgrond-attachment 无继承性 css1/css3
值：fixed:背景图相对于窗体固定
    local:背景图相对于元素固定
    scroll:背景图相对于元素内容固定

#background-orgin 无继承性 CSS3
background-origin：<box> [ , <box> ]*
<box> = border-box | padding-box | content-box
默认值：padding-box
值：padding-box： 从padding区域（含padding）开始显示背景图像。
    border-box： 从border区域（含border）开始显示背景图像。
    content-box：从content区域开始显示背景图像。

#background-clip 无继承性 CSS3
background-clip：<box> [ , <box> ]*
<box> = border-box | padding-box | content-box | text
默认值：border-box
值：
    padding-box：从padding区域（不含padding）开始向外裁剪背景。
    border-box：从border区域（不含border）开始向外裁剪背景。
    content-box：从content区域开始向外裁剪背景。
    text：从前景内容的形状（比如文字）作为裁剪区域向外裁剪，如此即可实现使用背景作为填充色之类的遮罩效果。

#background-size 无继承性 CSS3
background-size：<bg-size> [ , <bg-size> ]*
<bg-size> = [ <length> | <percentage> | auto ]{1,2} | cover | contain
默认值：auto
值：
<length>：用长度值指定背景图像大小。不允许负值。
<percentage>：用百分比指定背景图像大小。不允许负值。
auto：背景图像的真实大小。
cover：将背景图像等比缩放到完全覆盖容器，背景图像有可能超出容器。
contain：将背景图像等比缩放到宽度或高度与容器的宽度或高度相等，背景图像始终被包含在容器内。

#Multiple backgrond 无继承性 CSS3
可以定义多个背景图像，分别设置image\repeat\position\size\attachment\clip\origin
也可以写在一起，用逗号隔开

###颜色属性

#opacity 无继承性 CSS3
opacity：<number>
默认值：    1
值：0.1-1,指定对象的不透明度
对于IE8之前，使用filter:alpha(opacity:50);

#font-variant 无继承性 CSS3
值:normal
    small-caps:小型大写字母

#font-stretch 无继承性 CSS3
谷歌等暂不支持

