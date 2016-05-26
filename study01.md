###定位 position

###position 无继承性
static:无特殊定位，对象遵循正常的文档流，top等值无效

###z-index 无继承性
值：auto，继承父对象的定位
规则：并级的对象，此属性参数值越大，则被层叠在最上面。
      如两个对象的此属性具有同样的值，那么将依据它们在HTML文档中流的顺序层叠，写在后面的将会覆盖前面的。
      必须定义position属性值为absolute、relative或fixed，此取值方可生效。
      对应的脚本特性为zIndex。

###布局 layout 无继承性
##display 无继承性
值：table-cell,指定对象为块元素的表格，可以使用表格的特殊样式
兼容性：IE7及更早浏览器只支持none | inline | block | inline-block | list-item参数值。

##clear 无继承性
left:清除之前元素的左浮动影响，就相当于之前元素没有设置浮动
right:清除之前元素的右浮动影响，就相当于之前元素没有设置浮动
both:清除之前元素的左和右浮动影响，就相当于之前元素没有设置浮动

##visibility 无继承性
该属性与display不同，此属性为隐藏的对象保留其物理空间
值：collapse，对表格对象隐藏边框，对其他对象相当于hidden

##overflow 无继承性
值：visible 所有内容可视
    hidden:超出内容隐藏
    scroll：超出内容可以通过滚动条查看
    auto:需要时自动添加滚动条
类似的：overflow-x overflow-y

###弹性盒模型  CSS3

##box-orient 无继承性  
值：horizontal:设置弹性盒模型对象的子元素水平排列
    vertical：设置弹性盒模型对象的子元素为纵向排列



###边框 Border 

##border-image 无继承性 CSS3
border-image：border-image-source || border-image-slice? [ / border-image-width ?][ / border-image-outset? ] ] || [border-image-repeat]
border-image-source:图片地址
border-image-slice：图片做成边框的样式
border-image-repeat：图片的重复方式

##border-top-left-radius ...

##border-reflect  无继承性 CSS3 设置图片镜像/倒影
    box-reflect：none | <direction> <offset>? <mask-box-image>?
         <direction> = above | below | left | right
         <offset> = <length> | <percentage>
         <mask-box-image> = none | <url> | <linear-gradient> | <radial-gradient> | <repeating-linear-gradient> | <repeating-radial-gradient>
    默认值：none


###背景 background


##backgrond-attachment 无继承性 css1/css3
值：fixed:背景图相对于窗体固定
    local:背景图相对于元素固定
    scroll:背景图相对于元素内容固定

##background-orgin 无继承性 CSS3
background-origin：<box> [ , <box> ]*
<box> = border-box | padding-box | content-box
默认值：padding-box
值：padding-box： 从padding区域（含padding）开始显示背景图像。
    border-box： 从border区域（含border）开始显示背景图像。
    content-box：从content区域开始显示背景图像。

##background-clip 无继承性 CSS3
background-clip：<box> [ , <box> ]*
<box> = border-box | padding-box | content-box | text
默认值：border-box
值：
    padding-box：从padding区域（不含padding）开始向外裁剪背景。
    border-box：从border区域（不含border）开始向外裁剪背景。
    content-box：从content区域开始向外裁剪背景。
    text：从前景内容的形状（比如文字）作为裁剪区域向外裁剪，如此即可实现使用背景作为填充色之类的遮罩效果。

##background-size 无继承性 CSS3
background-size：<bg-size> [ , <bg-size> ]*
<bg-size> = [ <length> | <percentage> | auto ]{1,2} | cover | contain
默认值：auto
值：
<length>：用长度值指定背景图像大小。不允许负值。
<percentage>：用百分比指定背景图像大小。不允许负值。
auto：背景图像的真实大小。
cover：将背景图像等比缩放到完全覆盖容器，背景图像有可能超出容器。
contain：将背景图像等比缩放到宽度或高度与容器的宽度或高度相等，背景图像始终被包含在容器内。

##Multiple backgrond 无继承性 CSS3
可以定义多个背景图像，分别设置image\repeat\position\size\attachment\clip\origin
也可以写在一起，用逗号隔开

###颜色属性

##opacity 无继承性 CSS3
opacity：<number>
默认值：    1
值：0.1-1,指定对象的不透明度
对于IE8之前，使用filter:alpha(opacity:50);


###字体 font

##font-family 
语法：
font-family：[ <family-name> | <generic-family> ] [, <family-name> | <generic-family>]*
<family-name> = arial | georgia | verdana | helvetica | simsun and etc.
<generic-family> = cursive | fantasy | monospace | serif | sans-serif
默认值：由浏览器确定
<family-name>：字体名称。按优先顺序排列。以逗号隔开。如果字体名称包含空格或中文，则应使用引号括起
<generic-family>：字体序列名称。

font-family:'宋体',arial,georgia,verdana,helvetica,sans-serif;



##font-variant 无继承性 CSS3
值:normal
    small-caps:小型大写字母

##font-stretch 无继承性 CSS3
谷歌等暂不支持


###文本text


##text-overflow 无继承性 CSS3
text-overflow：clip | ellipsis
默认值：clip
clip：
当对象内文本溢出时不显示省略标记（...），而是将溢出的部分裁切掉。
ellipsis：
当对象内文本溢出时显示省略标记（...）。

##text-decoration-line 无继承性 CSS3  浏览器赞不支持
text-decoration-line：none | [ underline || overline || line-through ]
默认值：none

##text-decoration-color 无继承性 CSS3 浏览器赞不支持

##text-decoration-style 无继承性 CSS3  浏览器暂不支持
text-decoration-style：solid | double | dotted | dashed | wavy
默认值：solid
solid:实线
double：双线
dotted：点状线条
dashed：虚线
wavy：波浪线

##text-align
取值：
left：内容左对齐。
center：内容居中对齐。
right：内容右对齐。
justify：
内容两端对齐。写本文档时仅Firefox能看到正确效果
start：内容对齐开始边界。（CSS3）
end：内容对齐结束边界。（CSS3）

##text-decoration  暂不支持
取值：
[ text-decoration-line ]：指定文本装饰的种类。相当于CSS1时的text-decoration属性
[ text-decoration-style ]：指定文本装饰的样式。
[ text-decoration-color ]：指定文本装饰的颜色。
blink：指定文字的装饰是闪烁。写本文档时仅Firefox和Opera支持该参数值

##text-shadow 有继承性 CSS3
无阴影
<length>①：第1个长度值用来设置对象的阴影水平偏移值。可以为负值
<length>②：第2个长度值用来设置对象的阴影垂直偏移值。可以为负值
<length>③：如果提供了第3个长度值则用来设置对象的阴影模糊值。不允许负值
<color>：设置对象的阴影的颜色。
例：text-shadow:2px 3px 2px #333

#text-fill-color 有继承性  CSS3 多浏览器暂不支持
值：color值
指定文字的填充颜色
若同时设置text-fill-color和color，text-fill-color定义的颜色将覆盖color属性
要写成：-webkit-text-fill-color:red

##text-stroke
[ text-stroke-width ]:设置或检索对象中的文字的描边厚度
[ text-stroke-color ]：设置或检索对象中的文字的描边颜色
如：-webkit-text-stroke:2px #333

##text-stroke-width
##text-stroke-color

##word-wrap 有继承性  CSS3
normal：允许内容顶开或溢出指定的容器边界。
break-word：内容将在边界内换行。如果需要，单词内部允许断行。


###列表 list 

##list-style
取值：[ list-style-image ]：设置或检索作为对象的列表项标记的图像
[ list-style-position ]：设置或检索作为对象的列表项标记如何根据文本排列
[ list-style-type ]：设置或检索对象的列表项所使用的预设标记


###表格 table

##caption-side
top：指定caption在表格上边
bottom：指定caption在表格下边
eg.caption-side:bottom

##empty-cells
值：hide：指定当表格的单元格无内容时，隐藏该单元格的边框。
    show：指定当表格的单元格无内容时，显示该单元格的边框。
eg.empty-cells:hide;


##content CSS2
normal:默认值。表现与none值相同
none：不生成任何值。
<attr>：插入标签属性值
<url>：使用指定的绝对或相对地址插入一个外部资源（图像，声频，视频或浏览器支持的其他任何资源）
<string>：插入字符串
counter(name)：使用已命名的计数器
counter(name,list-style-type)：使用已命名的计数器并遵从指定的list-style-type属性
counters(name,string)：使用所有已命名的计数器
counters(name,string,list-style-type)：使用所有已命名的计数器并遵从指定的list-style-type属性
no-close-quote：并不插入quotes属性的后标记。但增加其嵌套级别
no-open-quote：并不插入quotes属性的前标记。但减少其嵌套级别
close-quote：
插入quotes属性的后标记
open-quote：
插入quotes属性的前标记

用来和:after及:before伪元素一起使用，在对象前或后显示内容。
eg.  .attr p:after{content:attr(title);}
     .url p:before{content:url(../../skin/ico.png);}


###用户界面


#outline outline画在border外面
[ outline-width ]：指定轮廓边框的宽度。
[ outline-style ]：指定轮廓边框的样式。
[ outline-color ]：指定轮廓边框的颜色。
eg. outline: 1px dashed #123546

#outline-offset CSS3 这个值不计算在元素所占区域大小
取值：<length>：用长度值来定义轮廓偏移(偏移边框)。不允许负值
eg. outline-offset:3px

##nav-index CSS3 浏览器暂不支持

##cursor 
cursor：[<url> [<x> <y>]?,]*[ auto | default | none | context-menu | help | pointer | progress | wait | cell | crosshair | text | vertical-text | alias | copy | move | no-drop | not-allowed | e-resize | n-resize | ne-resize | nw-resize | s-resize | se-resize | sw-resize | w-resize | ew-resize | ns-resize | nesw-resize | nwse-resize | col-resize | row-resize | all-scroll]
默认值：auto
定义光标类型


##zoom 
语法：
zoom：normal | <number> | <percentage>
默认值：normal
取值：
normal：使用对象的实际尺寸。
<number>：用浮点数来定义缩放比例。不允许负值
<percentage>：用百分比来定义缩放比例。不允许负值

##box-sizing 无继承性 CSS3
语法：
box-sizing：content-box | border-box
默认值：content-box
取值：
content-box：padding和border不被包含在定义的width和height之内。对象的实际宽度等于设置的width值和border、padding之和，即 ( Element width = width + border + padding )
此属性表现为标准模式下的盒模型。
border-box：padding和border被包含在定义的width和height之内。对象的实际宽度就等于设置的width值，即使定义有border和padding也不会改变对象的实际宽度，即 ( Element width = width )
此属性表现为怪异模式下的盒模型。

##resize  无继承性  CSS3：
语法：
resize：none | both | horizontal | vertical
默认值：none
取值：
none：不允许用户调整元素大小。
both：用户可以调节元素的宽度和高度。
horizontal：用户可以调节元素的宽度
vertical：用户可以调节元素的高度

如果希望此属性生效，需要设置对象的overflow属性，值可以是auto,hidden或scroll。
eg. resize:both;
    overflow:hidden;

##ime-mode 无继承性 CSS3
语法：
zoom：auto | normal | active | inactive | disabled
默认值：auto
取值：
auto：不影响IME的状态。
normal：正常的IME状态
active：指定所有使用ime输入的字符。即激活本地语言输入法。用户仍可以撤销激活ime
inactive：指定所有不使用ime输入的字符。即激活非本地语言。用户仍可以撤销激活ime
disabled：完全禁用ime。对于有焦点的控件(如输入框)，用户不可以激活ime

设置或检索是否允许用户激活输入中文，韩文，日文等的输入法（IME）状态。


###多列 Multi-column

columns 无继承性：CSS3
语法：
columns：[ column-width ] || [ column-count ]
默认值：看每个独立属性
取值：
[ column-width ]：设置或检索对象每列的宽度
[ column-count ]：设置或检索对象的列数
说明：
设置或检索对象的列数和每列的宽度。复合属性
eg. -webkit-columns:100px 3;
    -webkit-columns:5;

##column-count 无继承性 CSS3
语法：
column-count：<integer> | auto
默认值：auto
取值：
<integer>：用整数值来定义列数。不允许负值
auto：根据column-width自定分配宽度
说明：
设置或检索对象的列数

##column-gap 无继承性  CSS3 ：
语法：
column-gap：<length> | normal
默认值：normal
取值：
<length>：
用长度值来定义列与列之间的间隙。不允许负值
normal：
与font-size大小相同。假设该对象的font-size为16px，则normal值为16px，类推。
说明：
设置或检索对象的列与列之间的间隙

##column-rule 无继承性 CSS3
语法：
column-rule：[ column-rule-width ] || [ column-rule-style ] || [ column-rule-color ]
默认值：看每个独立属性
取值：
[ column-rule-width ]：设置或检索对象的列与列之间的边框厚度。
[ column-rule-style ]：设置或检索对象的列与列之间的边框样式。
[ column-rule-color ]：设置或检索对象的列与列之间的边框颜色。
说明：
设置或检索对象的列与列之间的边框。复合属性。参阅border属性
eg. -webkit-column-rule:3px dashed #333

##column-span 无继承性 CSS3 应为块级元素设置才有效果
语法：
column-span：none | all
默认值：none
取值：
none：不跨列
all：横跨所有列
说明：
设置或检索对象元素是否横跨所有列。
<p style="-webkit-column-span:all;background-color:red">的时候Activity已经过on,到onStart经,到onStart经,到onStart经Resume,</p>

##column-fill 无继承性 CSS3
语法：
column-fill：auto | balance
默认值：auto
取值：
auto：列高度自适应内容
balance：所有列的高度以其中最高的一列统一
说明：
设置或检索对象所有列的高度是否统一。

##column-break-before CSS3继承性：无
语法：
column-break-before：auto | always | avoid | left | right | page | column | avoid-page | avoid-column
默认值：auto
取值：
auto：既不强迫也不禁止在元素之前断行并产生新列
always：总是在元素之前断行并产生新列
avoid：避免在元素之前断行并产生新列
说明：
设置或检索对象之前是否断行。

####column-break-after
####column-break-inside


###变换 transform

##transform-origin版本：CSS3继承性：无
语法：
transform-origin：[ <percentage> | <length> | left | center① | right ] [ <percentage> | <length> | top | center② | bottom ]?
默认值：50% 50%，效果等同于center center
取值：
<percentage>：用百分比指定坐标值。可以为负值。
<length>：用长度值指定坐标值。可以为负值。
left：指定原点的横坐标为left
center①：指定原点的横坐标为center
right：指定原点的横坐标为right
top：指定原点的纵坐标为top
center②：指定原点的纵坐标为center
bottom：指定原点的纵坐标为bottom
说明：
设置或检索对象以某个原点进行转换。

##transform版本：CSS3继承性：无
语法：
transform：none | matrix(<number>,<number>,<number>,<number>,<number>,<number>)? translate(<length>[,<length>])? translateX(<length>)? translateY(<length>)? rotate(<angle>)? scale(<number>[,<number>])? scaleX(<number>)? scaleY(<number>)? skew(<angle>[,<angle>])? skewX(<angle>) || skewY(<angle>)?
默认值：none
取值：
none：无转换
matrix(<number>,<number>,<number>,<number>,<number>,<number>)：
以一个含六值的(a,b,c,d,e,f)变换矩阵的形式指定一个2D变换，相当于直接应用一个[a,b,c,d,e,f]变换矩阵
translate(<length>[, <length>])：指定对象的2D translation（2D平移）。第一个参数对应X轴，第二个参数对应Y轴。如果第二个参数未提供，则默认值为0
translateX(<length>)：指定对象X轴（水平方向）的平移
translateY(<length>)：指定对象Y轴（垂直方向）的平移
rotate(<angle>)：指定对象的2D rotation（2D旋转），需先有transform-origin属性的定义
scale(<number>[, <number>])：指定对象的2D scale（2D缩放）。第一个参数对应X轴，第二个参数对应Y轴。如果第二个参数未提供，则默认取第一个参数的值
scaleX(<number>)：指定对象X轴的（水平方向）缩放
scaleY(<number>)：指定对象Y轴的（垂直方向）缩放
skew(<angle> [, <angle>])：指定对象skew transformation（斜切扭曲）。第一个参数对应X轴，第二个参数对应Y轴。如果第二个参数未提供，则默认值为0
skewX(<angle>)：指定对象X轴的（水平方向）扭曲
skewY(<angle>)：指定对象Y轴的（垂直方向）扭曲
说明：
设置或检索对象的转换。

###转换 transition
transition版本：CSS3继承性：无
语法：
transition：[ transition-property ] || [ transition-duration ] || [ transition-timing-function ] || [ transition-delay ]
默认值：看每个独立属性
取值：
[ transition-property ]：检索或设置对象中的参与过渡的属性
[ transition-duration ]：检索或设置对象过渡的持续时间
[ transition-timing-function ]：检索或设置对象中过渡的动画类型
[ transition-delay ]：检索或设置对象延迟过渡的时间
说明：
复合属性。检索或设置对象变换时的过渡。

eg. -webkit-transition:background-color 3s ease-in 0.5s;
    background-color:red

    -webkit-transition:background-color 3s ease-in 0.5s,border 1s ease-in 0.5s;
    background-color:red;
    border:1px solid blue;

##transition-property 无继承性 CSS3
语法：
transition-property：all | none | <property>[ ,<property> ]*
默认值：all
取值：
all：所有可以进行过渡的css属性
none：不指定过渡的css属性
<property>：指定要进行过渡的css属性
说明：
检索或设置对象中的参与过渡的属性。
默认值为：all。默认为所有可以进行过渡的css属性。
如果提供多个属性值，以逗号进行分隔。
eg.  -webkit-transition:all 3s ease-in 0.5s;
     background-color:red;
     border:1px solid blue;

##transition-duration 无继承性 CSS3
语法：
transition-duration：<time>[ ,<time> ]*
默认值：0
取值：
<time>：
指定对象过渡的持续时间
说明：
检索或设置对象过渡的持续时间。
如果提供多个属性值，以逗号进行分隔。

eg.  -webkit-transition-duration:.5s;
      left:300px;

##transition-timing-function 无继承性 CSS3
语法：
transition-timing-function：linear | ease | ease-in | ease-out | ease-in-out | cubic-bezier(<number>, <number>, <number>, <number>)[ ,linear | ease | ease-in | ease-out | ease-in-out | cubic-bezier(<number>, <number>, <number>, <number>) ]*
默认值：ease
取值：
linear：线性过渡。等同于贝塞尔曲线(0.0, 0.0, 1.0, 1.0)
ease：平滑过渡。等同于贝塞尔曲线(0.25, 0.1, 0.25, 1.0)
ease-in：由慢到快。等同于贝塞尔曲线(0.42, 0, 1.0, 1.0)
ease-out：由快到慢。等同于贝塞尔曲线(0, 0, 0.58, 1.0)
ease-in-out：由慢到快再到慢。等同于贝塞尔曲线(0.42, 0, 0.58, 1.0)
cubic-bezier(<number>, <number>, <number>, <number>)：
特定的贝塞尔曲线类型，4个数值需在[0, 1]区间内
说明：
检索或设置对象中过渡的动画类型。
如果提供多个属性值，以逗号进行分隔

##transition-delay 无继承性 CSS3 
语法：
transition-delay：<time>[ ,<time> ]*
默认值：0
取值：
<time>：指定对象过渡的延迟时间
说明：
检索或设置对象延迟过渡的时间。
如果提供多个属性值，以逗号进行分隔。


###动画 animation

##animation 无继承性 CSS3 
语法：
animation：[[ animation-name ] || [ animation-duration ] || [ animation-timing-function ] || [ animation-delay ] || [ animation-iteration-count ] || [ animation-direction ]] [ , [ animation-name ] || [ animation-duration ] || [ animation-timing-function ] || [ animation-delay ] || [ animation-iteration-count ] || [ animation-direction ]]*
默认值：看每个独立属性
相关属性：[ animation-play-state ]
取值：
[ animation-name ]：检索或设置对象所应用的动画名称
[ animation-duration ]：检索或设置对象动画的持续时间
[ animation-timing-function ]：检索或设置对象动画的过渡类型
[ animation-delay ]：检索或设置对象动画延迟的时间
[ animation-iteration-count ]：检索或设置对象动画的循环次数
[ animation-direction ]：检索或设置对象动画在循环中是否反向运动
[ animation-play-state ]：检索或设置对象动画的状态。w3c正考虑是否将该属性移除，因为动画的状态可以通过其它的方式实现，比如重设样式
说明：
复合属性。检索或设置对象所应用的动画特效。
如果提供多组属性值，以逗号进行分隔。

##animation-fill-mode版本：CSS3继承性：无
语法：
animation-fill-mode：none | forwards | backwards | both [ , none | forwards | backwards | both ]*
默认值：none
取值：
none：默认值。不设置对象动画之外的状态
forwards：设置对象状态为动画结束时的状态
backwards：设置对象状态为动画开始时的状态
both：设置对象状态为动画结束或开始的状态
说明：
检索或设置对象动画时间之外的状态
如果提供多个属性值，以逗号进行分隔。

##animation-iteration-count版本：CSS3继承性：无
语法：
animation-iteration-count：infinite | <number> [ , infinite | <number> ]*
默认值：1
取值：
infinite：无限循环
<number>：指定对象动画的具体循环次数

###媒体查询  Media Queries


##media features width    CSS3 是否接受min/max：是
语法：
width：<length>
取值：
<length>：用长度值来定义宽度。不允许负值
说明：
定义输出设备中的页面可见区域宽度。
与盒模型width不同，媒体特性width的取值只能是<length>。
本特性接受min和max前缀，因此可以派生出min-width和max-width两个媒体特性。
eg. @media all and (min-width:500px) and (max-width:1000px){
        body{color:#f00;}
    }

##media features height CSS3 是否接受min/max：是
语法：
height：<length>
取值：
<length>：用长度值来定义高度。不允许负值
说明：
定义输出设备中的页面可见区域高度。
与盒模型height不同，媒体特性height的取值只能是<length>。
本特性接受min和max前缀，因此可以派生出min-height和max-height两个媒体特性。
eg. @media all and (min-height:200px) and (max-height:1000px){
        ul li{background-color:#f00;}
    }


##media features device-width版本：CSS3是否接受min/max：是
语法：
device-width：<length>
取值：
<length>：用长度值来定义宽度。不允许负值
说明：
定义输出设备的屏幕可见宽度。
本特性接受min和max前缀，因此可以派生出min-device-width和max-device-width两个媒体特性。

eg. @media screen and (device-width:1024px){
        body{color:#f00;}
    }



###图像类型取值 Image Type


##linear-gradient()版本：CSS3
语法：
<linear-gradient>：linear-gradient([ <point>,]? <color-stop>[, <color-stop>]+);
<point>：[ left | right ]? [ top | bottom ]? || <angle>?
<color-stop>：<color> [ <length> | <percentage> ]?
取值：
<point>
left：设置左边为渐变起点的横坐标值。
right：设置右边为渐变起点的横坐标值。
top：设置顶部为渐变起点的纵坐标值。
bottom：设置底部为渐变起点的纵坐标值。
<angle>：用角度值指定渐变的方向（或角度）。
<color-stop>：指定渐变的起止颜色。
<color-stop>
<color>：指定颜色。请参阅颜色值
<length>：用长度值指定起止色位置。不允许负值
<percentage>：用百分比指定起止色位置。
说明：
用线性渐变创建图像。
写本文档时Firefox,Chrome,Opera已经在实验性质阶段支持了该属性，Safari对该属性的支持仍停留在以私有方式实现的阶段（可参阅页面底部的示例代码）。
Firefox还支持使用<percentage>、<length>和center特殊值定义渐变起点，并支持起点与角度一起使用。

##radial-gradient()
##repeating-linear-gradient()
##repeating-radial-gradient()























