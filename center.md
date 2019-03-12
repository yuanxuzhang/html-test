# 居中
## 水平居中  
### 行内元素  
* **父元素**是**块级**元素，直接给父元素设置 text-align: center。  
[code](./center/horizontalLineWithBlockParentTest.html)  
* **父元素**不是**块级**元素，则先将其父元素设置为块级元素，再给父元素设置 text-align: center;  
[code](./center/horizontalLineWithBlockParentTest.html)  
### 块级元素  
#### 方案一  
* 宽度已知：需要谁居中，给其设置 margin: 0 auto; （作用：使盒子自己居中）  
[code](./center/horizontalBlockWithMarginAndNumberTest.html)  
[code](./center/horizontalBlockWithMarginAndPercentageTest.html)  
* 宽度未知：默认子元素的宽度和父元素一样，这时需要设置子元素为display: inline-block; 或 display: inline;即将其转换成行内块级/行内元素，给父元素设置 text-align: center; 
[code](./center/horizontalBlockUnknowWidthAndHeightTest.html)  
#### 方案二  
设置父元素为相对定位，再设置子元素为绝对定位，设置子元素的left:50%，即让子元素的左上角水平居中； 
* 宽高已知：使用定位属性  
[code](./center/horizontalWithPositionKnowWidthAndHeight.html)  
* 宽高未知：利用css3新增属性transform: translateX(-50%)    
[code](./center/horizontalBlockUnknowWidthAndHeightTest.html)  
#### 方案三：使用flexbox布局实现（宽度定不定都可以） 
使用flexbox布局，只需要给待处理的块状元素的父元素添加属性 display: flex; justify-content: center;  
[code](./center/horizontalBlockWithFlex.html)  
## 垂直居中  
### 单行的行内元素  
需要设置单行行内元素的"行高等于盒子的高"即可*line-height可设置数字和百分比（相对于字体）*  
[code](./center/verticalLineWithLineHeight.html)  
### 多行的行内元素  
使用给父元素设置**display:table-cell**;和vertical-align: middle;属性即可；   
PS： 亦可适用于单行   
[code](./center/verticalMultiLineWithLineHeight.html)  
### 块级元素  
#### 方案一：使用定位  
设置父元素为相对定位，再设置子元素为绝对定位，设置子元素的top: 50%，即让子元素的左上角垂直居中  
* 宽高已知：设置绝对子元素的 margin-top: -元素高度的一半px; 或者设置transform: translateY(-50%)  
[code](./center/verticalBlockWithLineHeight.html)    
* 宽高未知：利用css3新增属性transform: translateY(-50%)  
[code](./center/verticalBlockWithPositionUnkonwLineHeight.html)  
#### 方案二：使用flexbox布局实现（高度定不定都可以）  
使用flexbox布局，只需要给待处理的块状元素的父元素添加属性 display: flex; align-items: center  
[code](./center/verticalLineWithFlex.html)  
##  水平垂直居中  
### 已知高度和宽度的元素  
#### 方案一：设置父元素为相对定位，给子元素设置绝对定位，top: 0; right: 0; bottom: 0; left: 0; margin: auto;  
[code](./center/horizontalAndVerticalWithPostionAndMargin.html)  
#### 方案二：设置父元素为相对定位，给子元素设置绝对定位，left: 50%; top: 50%; margin-left: --元素宽度的一半px; margin-top: --元素高度的一半px;   
[code](./center/horizontalAndVerticalWithPostionAndMargin2.html)    
### 未知高度和宽度的元素  
#### 方案一：使用定位属性
设置父元素为相对定位，给子元素设置绝对定位，left: 50%; top: 50%; transform: translateX(-50%) translateY(-50%);  
[code](./center/horizontalAndVerticalWithPostionAndMarginUnknowWidthAndHeight.html)    
### 使用flex布局实现  
设置父元素为flex定位，justify-content: center; align-items: center;  
[code](./center/horizontalAndVerticalWithFlex.html)  

## refered  
[CSS水平居中+垂直居中+水平/垂直居中的方法总结](https://blog.csdn.net/weixin_37580235/article/details/82317240)  
