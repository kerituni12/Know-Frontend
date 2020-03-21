## CSS (Cascading Style Sheets)
> CSS is a language that describes the style and how HTML element should be displayed

The “cascading” in CSS refers to the fact that styling rules “cascade” down from several sources. This means that CSS has an inherent hierarchy and styles of a higher precedence will overwrite rules of a lower precedence.

## CSS Selector

One ex for all https://www.w3schools.com/cssref/trysel.asp?selector=p:first-of-type

- Simple ( name, id, class)
- Combinator ( relationship between them )
- Pseudo-class (certain state)
- Pseudo-elements (select and style a part of an element)
- Attribute (attribute or attribute value)

4 Combinators (tổ hợp)  
- descendant(con cháu) selector                      (space)  
- child selector                                     (>)       (all child level 1)     
- adjacent(liền kề) sibling(cùng cha)                (+)       (only first e adjacent)
- general(chung) sibling                             (~)       (all element sibling) 

https://www.w3schools.com/css/css_selectors.asp

Pesudo element 

- Style the first letter, or line, of an element
- Insert content before, or after, the content of an element

::after
::before
::first-letter
::first-line
::marker
::placeholder
::selection

Tạo chữ hoa đàu dòng, đổi màu chữ select, ...

Pseudo Class

https://www.w3schools.com/css/css_pseudo_elements.asp

First child vs first of type
https://jsfiddle.net/bwLvyf3k/1/

Ex :nth-of-type(odd)

CSS Attribute Selectors

[attribute="value"]  a specified attribute and value.
[attribute~="value"] an attribute value containing a specified word
[attribute|="value"] specified attribute starting with the specified value.(-)
[attribute^="value"] begin with specified value
[attribute$="value"] end
[attribute*="value"] attribute value contains a specified value


CSS RGBA Value
rgba(red, green, blue, alpha)

//  CSS Backgroud 

background	        Sets all the background properties in one declaration
background-attachment	Sets whether a background image is fixed or scrolls with the rest of the page
background-color	Sets the background color of an element
background-image	Sets the background image for an element
background-position	Sets the starting position of a background image
background-repeat	Sets how a background image will be repeated
background-blend-mode   the blending mode of each background layer 

CSS Multiple Backgrounds

background-clip	        Specifies the painting area of the background
background-origin	Specifies where the background image(s) is/are positioned
background-size	        Specifies the size of the background image(s)

transparent : trong suốt

Margin Vs Padding (Canh lề ngoài , canh lề trong)

Outline nằm ngoài margin

Text Properties
indent : thụt dòng
letter-spacing: khoảng cách giữa các kí tự 
word-spacing: kc từ
line-height: khoảng cách dòng 
direction: phương hướng kết hợp unicode-bidi(đảo ngược thứ tự)
vertical-align: canh theo chiều dọc
text-transform: chuyển đổi chữ

Block vs inline vs inline-block (100% width - 1 dòng - 1 dòng và có thuộc tính của block)

https://viblo.asia/p/su-khac-nhau-giua-display-inline-block-va-inline-block-oOVlYNon58W

CSS position
static
relative    The element is positioned relative to its normal position
fixed
absolute    The element is positioned relative to its first positioned (not static) ancestor element
sticky      = relative + fixed

https://medium.com/@leannezhang/difference-between-css-position-absolute-versus-relative-35f064384c6

Float and clearfix
https://hocwebchuan.com/tutorial/tut_css_clearfix.php
https://css-tricks.com/clearfix-a-lesson-in-web-development-evolution/

.container {
  display: flow-root;
}

.clearfix::after {
  content: "";
  clear: both;
  display: table;
}


## CSS Align 

Margin auto rules
(display: block AND width not auto) OR display: table
float: none
position: relative

6 Trick to align 
https://www.hongkiat.com/blog/css-tricks-vertical-align-content/


## CSS Units

https://www.w3schools.com/css/css_units.asp

## CSS Specificity

https://www.w3schools.com/css/css_specificity.asp

- Specificity Hierarchy
- Equal specificity: the latest rule counts
- ID selectors have a higher specificity than attribute selectors
- Contextual selectors are more specific than a single element selector ( external CSS file < in HTML)
- A class selector beats any number of element selectors 
- The universal selector and inherited values have a specificity of 0 ( *, body *)

CSS GRadients

Linear Gradients (goes down/up/left/right/diagonally)
Radial Gradients (defined by their center)

CSS Text Effects

text-overflow                       kết hợp white-space: nowrap; 
word-wrap long word                 ngắt từ vượt quá chiều rộng
word-break                          phủ tràn chiều rộng

CSS Transform 
translate() dịch chuyển 
rotate()    xoay
scale(), X, Y     thu phóng
skew(), X , Y      nghiêng
matrix()    matrix(scaleX(),skewY(),skewX(),scaleY(),translateX(),translateY())

3d
rotateX()
rotateY()
rotateZ()

transform-origin	        Allows you to change the position on transformed elements
transform-style	                Specifies how nested elements are rendered in 3D space
perspective (góc nhìn cá nhân)	Specifies the perspective on how 3D elements are viewed
perspective-origin	        Specifies the bottom position of 3D elements
backface-visibility	        Defines whether or not an element should be visible when not facing the screen

CSS Transitions

transition
transition-delay (độ trễ)
transition-duration (thời lượng)
transition-property
transition-timing-function

ease - specifies a transition effect with a slow start, then fast, then end slowly (this is default)
linear - specifies a transition effect with the same speed from start to end
ease-in - specifies a transition effect with a slow start
ease-out - specifies a transition effect with a slow end
ease-in-out - specifies a transition effect with a slow start and end
cubic-bezier(n,n,n,n) - lets you define your own values in a cubic-bezier function

Transition + Transformation

CSS Animation

@keyframes
animation-name
animation-duration
animation-delay
animation-iteration-count  số lần lặp
animation-direction
animation-timing-function
animation-fill-mode
animation