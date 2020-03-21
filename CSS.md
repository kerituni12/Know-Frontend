## CSS (Cascading Style Sheets)
> CSS is a language that describes the style and how HTML element should be displayed

The “cascading” in CSS refers to the fact that styling rules “cascade” down from several sources. This means that CSS has an inherent hierarchy and styles of a higher precedence will overwrite rules of a lower precedence.

## CSS Selector

https://www.w3schools.com/cssref/css_selectors.asp

One ex for all https://www.w3schools.com/cssref/trysel.asp?selector=p:first-of-type

- Simple ( name, id, class)
- Combinator ( relationship between them )
- Pseudo-class (certain state)
- Pseudo-elements (select and style a part of an element)
- Attribute (attribute or attribute value)

4 Combinators (tổ hợp)  
- descendant(con cháu) selector                      (space)  
- child selector                                     (>)       (all child level 1)     
- adjacent(liền kề) sibling(cùng cha, anh chị em)    (+)       (only first e adjacent | immediately after)
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

Em vs rem
https://webdesign.tutsplus.com/tutorials/comprehensive-guide-when-to-use-em-vs-rem--cms-23984

## CSS Specificity

SPECIFICITY IS A COMMON REASON WHY YOUR CSS-RULES DON’T APPLY TO SOME ELEMENTS, ALTHOUGH YOU THINK THEY SHOULD.

https://www.w3schools.com/css/css_specificity.asp

Specificity Hierarchy

Inline styles > IDs > Classes, attributes và pseudo-classes > Elements and pseudo-elements

User Agent Styles (browser) < User Styles < Auther Styles

// A user style sheet is an assistive tool that allows users to customize the display of web content by writing their own CSS to override a site author’s styles
 
1000 for style attribute
100  for each ID, 
10   for each attribute, class or pseudo-class, 
1    for each element name or pseudo-element.

Specificity Rules

- Equal specificity: the latest rule counts
- ID selectors have a higher specificity than attribute selectors
- Contextual selectors are more specific than a single element selector ( external CSS file < in HTML)
- A class selector beats any number of element selectors 
- The universal selector and inherited values have a specificity of 0 ( *, body *)

Examples:

*               /* a=0 b=0 c=0 -> specificity =   0 */
LI              /* a=0 b=0 c=1 -> specificity =   1 */
UL LI           /* a=0 b=0 c=2 -> specificity =   2 */
UL OL+LI        /* a=0 b=0 c=3 -> specificity =   3 */
H1 + *[REL=up]  /* a=0 b=1 c=1 -> specificity =  11 */
UL OL LI.red    /* a=0 b=1 c=3 -> specificity =  13 */
LI.red.level    /* a=0 b=2 c=1 -> specificity =  21 */
#x34y           /* a=1 b=0 c=0 -> specificity = 100 */
#s12:not(FOO)   /* a=1 b=0 c=1 -> specificity = 101 */
#xxx > .a.b.c.d.e.f.g.h.i.j
#xxx < #xxx.a


## CSS GRadients

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

transition-timing-function property

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

animation-direction property

normal - The animation is played as normal (forwards). This is default
reverse - The animation is played in reverse direction (backwards)
alternate - The animation is played forwards first, then backwards
alternate-reverse - The animation is played backwards first, then forwards

animation-fill-mode property

none - Default value. Animation will not apply any styles to the element before or after it is executing
forwards - The element will retain the style values that is set by the last keyframe (depends on animation-direction and animation-iteration-count)
backwards - The element will get the style values that is set by the first keyframe (depends on animation-direction), and retain this during the animation-delay period
both - The animation will follow the rules for both forwards and backwards, extending the animation properties in both directions


CSS IMG style

https://www.w3schools.com/css/tryit.asp?filename=trycss_ex_images_filters
https://www.w3schools.com/cssref/css3_pr_filter.asp

CSS Multiple Columns

column-count
column-gap          khoảng cách column
column-rule-style
column-rule-width
column-rule-color
column-rule
column-span
column-width
https://www.w3schools.com/css/css3_multiple_columns.asp

CSS User Interface

resize 
outline 

CSS Variables

CSS Flexbox

flex-direction                             ( column, column-reverse, row, row-reverse)
flex-wrap (tự động xuống dòng)             ( wrap, wrap-reverse)
flex-flow shorthand direction + wrap 
justify-content	                            (flex-end, flex-start, space-round, space-between)
align-content

Items
flex-grow                                   khoảng chiếm giữ
flex-shrink                                 co lại 
align-seft

tab order

https://codepen.io/enxaneta/pen/adLPwv
https://css-tricks.com/snippets/css/a-guide-to-flexbox/

https://www.youtube.com/playlist?list=PLC3y8-rFHvwg6rjbiMadCILrjh7QkvzoQ

justify-content — controls alignment of all items on the main axis.
align-items — controls alignment of all items on the cross axis.
align-self — controls alignment of an individual flex item on the cross axis.
align-content — described in the spec as for “packing flex lines”; controls space between flex lines on the cross axis.

align-content xác định khoảng cách giữa các dòng, trong khi align-item xác định cách các mục tổng thể được căn chỉnh trong container. Khi chỉ có một dòng, nội dung căn chỉnh không có hiệu lực

CSS Media Queries


CSS grid

https://gridbyexample.com/examples/

grid-template-rows
grid-template-columns
grid-template-areas
grid-auto-rows               set default value for row
grid-auto-columns
grid-auto-flow                auto-placed items get inserted in the grid. (dense)

gird-area shorthand property for the grid-row-start, grid-column-start, grid-row-end and the grid-column-end properties.

fr unit 

CSS FUNCTION

https://www.w3schools.com/cssref/css_functions.asp

CSS Aural Reference 

use a combination of speech synthesis and sound effects to make the user listen to information, instead of reading information.
https://www.w3schools.com/cssref/css_ref_aural.asp 	


CSS Defaults values
https://www.w3schools.com/cssref/css_default_values.asp


CSS Entities

display any of these characters in HTML, you can use the CSS entity found in the table below.
https://www.w3schools.com/cssref/css_entities.asp

Web Safe Font


CSS Shapes
CSS Shapes cho phép các nhà thiết kế web tạo ra các bố cục hình học trừu tượng hơn, vượt ra ngoài các hình chữ nhật và hình vuông đơn giản
https://drafts.csswg.org/css-shapes/

Rules
only work k with float
content wil never flow on more than one side (k chay qua nhieu phia)

shape outside
clip path (part of the masking module, not part of the shapes spec) thay the cho clip

inset(l t r b round length)
circle(r at cx cy) 
ellipse(rx ry at cx cy)
polygon(x1 y1, x2 y2, …)


Masking vs clipping 
https://css-tricks.com/masking-vs-clipping-use/

https://bennettfeely.com/clippy/

https://css-tricks.com/clipping-masking-css/


svg vs canvas