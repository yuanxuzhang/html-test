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
* 宽度已知：使用定位属性  
[code](./center/horizontalWithPositionKnowWidthAndHeight.html)  
* 宽度未知：利用css3新增属性transform: translateX(-50%)  
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
