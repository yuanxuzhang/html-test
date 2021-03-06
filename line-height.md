##  定义和用法
line-height 属性设置**行间**的距离（行高）。
注释：不允许使用负值。

##  说明
该属性会影响**行框**的布局。在应用到一个块级元素时，它定义了该元素中基线之间的最小距离而不是最大距离。

line-height 与 font-size 的计算值之差（在 CSS 中成为“行间距”）分为两半，分别加到一个文本行内容的顶部和底部。可以包含这些内容的最小框就是行框。

原始数字值指定了一个缩放因子，后代元素会继承这个缩放因子而不是计算值。  

##  可能的值
值     	描述  
normal	 默认。设置合理的行间距。  
number	 **设置数字，此数字会与当前的字体尺寸相乘来设置行间距。**  
length	 设置固定的行间距。  
%	       **基于当前字体尺寸的百分比行间距。**  
inherit	 规定应该从父元素继承 line-height 属性的值。  

##  行元素 垂直居中技巧：设置line 的相对于字体的倍数值实现垂直居中。  
