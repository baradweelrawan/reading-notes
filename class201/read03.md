# this is read03 from 201
# Lists :
There are lots of occasions when we need to use lists. HTML provides us with three different types:
  1. Ordered lists
  2. Unordered lists
  3. Definition lists
# Ordered Lists : 
are lists where each item in the list is numbered. it is created with the 
1. <ol> element  
2. <li>
Each item in the list is placed between an opening <li> tag and a closing </li> tag.
# Unordered Lists :
are lists that begin with a bullet point rather than characters that indicate order.  it is created with the
1.  <ul> element.
2. <li> :Each item in the list is placed between an opening <li> tag
and a closing </li> tag. 
# Definition Lists: 
are made up of a set of terms along with the definitions for each of those terms.The definition list is created with the 
1. <dl> element and usually  consists of a series of terms and their definitions.Inside the <dl> element you will usually see pairs of <dt> and <dd> elements.
2. <dt> This is used to contain the term being defined the definition
term.
3. <dd> This is used to contain the definition.
# Nested Lists :
You can put a second list inside an <li> element to create a sublist
or nested list.
# Boxes: 
![img](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSJuh1qEMd_MpdRex3iJD5BNIcGb55K5ayG3w&usqp=CAU)

# Box Dimensions :
1. width, height :By default a box is sized just big enough to hold its contents. To set your own dimensions for a box you can use the height and width properties.The most popular ways to specify the size of a box are to use pixels, percentages, or ems.
# Limiting Width :
1. min-width:property specifies the smallest size a box can be displayed at when the browser window is narrow.
2.  max-width : property indicates the maximum width a box can stretch to when the browser window is wide.
# Overflowing Content :
1. overflow: tells the browser what to do if the content contained within a box is larger than the box itself. It can have one of two values:
  * hidden : hides any extra content that does not fit in the box.
  * scroll : adds a scrollbar to the box so that users can scroll 
to see the missing content.
# Border, Margin & Padding :
Every box has three available properties that can be adjusted to control its appearance: 
   1.  Border: Every box has a border even if it is not visible or is specified to be 0 pixels wide. The border separates the edge of one box from another.
   2. Margin : Margins sit outside the edge of the border. You can set the width of a margin to create a gap between the borders of two adjacent boxes.
   3. Padding :Padding is the space between the border of a box and any content contained within it. Adding padding can increase the readability of its contents.
   # White space & Vertical Margin:
   The padding and margin properties are very helpful in adding space between various items on the page.
   # Border Width :
   is used to control the width of a border. The value of this property can either be given in pixels or using one of the following values:thin ,medium,thick.You can control the individual size of borders using four separate properties: border-top-width,order-right-width,border-bottom-width,border-left-width.
   # Border Style :
   You can control the style of a border using the border-style property. This property can take the following values:
   1. solid a single solid line
   2. dotted a series of square dots if your border is 2px wide, then the dots are 2px squared with a 2px gap between each dot.
3. dashed a series of short lines
4. double two solid lines the value of the border-width property creates the sum of the two lines.
4. groove appears to be carved into the page.
5. ridge appears to stick out from the page.
6. inset appears embedded into the page.
# Border Color :
You can specify the color of a border using either RGB values,
hex codes or CSS color names.It is possible to individually
control the colors of the borders on different sides of a box using: border-top-color,border-right-color,border-bottom-color,border-left-color.
# Shorthand:
1. border:allows you to specify the width, style and color of a border in one property and the values should be coded in that specific order.
# padding :
allows you to specify how much space should appear between the
content of an element and its border.The value of this property is
most often specified in pixels.
# margin :
controls the gap between boxes. Its value is commonly given in pixels,
although you may also use percentages or ems.
# Centering Content :
If you want to center a box on the page or center it inside the element that it sits in, you can set the left-margin and right-margin to auto.to center a box on the page, you need to set a width for the box otherwise it will take up the full width of the page.
# Change Inline/Block :
1. display: allows you to turn an inline element  into a block-level element or vice versa, and can also be used to hide an element from the page. The values this property can take are:
  * inline: This causes a block-level element to act like an inline element.
  * block: This causes an inline element to act like a block-level element.
  * inline-block: This causes a block-level element to flow like an inline element, while retaining other features of a block-level element.
  * none :This hides an element from the page. In this case, the element
acts as though it is not on the page at al,although a user could
still see the content of the box if they used the view source option
in their browser.
# Hiding Boxes :
1. visibility : allows you to hide boxes from users but It leaves a pace where the element would have been.This property can take two
values:
  * hidden:This hides the element.
  * visible: This shows the element.
# Border Images :
applies an image to the border of any box. It takes a background image and slices it into nine pieces. This property requires three
pieces of information:
1. The URL of the image
2. Where to slice the image
3. 3: What to do with the straight edges; the possible values are
#  Box Shadows :
allows you to add a drop shadow around a box. It works just like the text-shadow property that you met on page 288. It must use at least the first of these two values as well as a color:
1. Horizontal offset Negative values position the shadow to the left of the box.
2. Vertical offset Negative values position the shadow to the top of the box.
3. Blur distance If omitted, the shadow is a solid line like a border.
4. Spread of shadow If used, a positive value will cause the shadow to expand in all directions, and a negative value will make it contract.
#  Rounded Corners:
* border-radius :The value
indicates the size of the radius in pixels.The -moz-border-radius
and -webkit-border-radius properties are not in the CSS specification.
#  Elliptical Shapes:
* border-radius :To create more complex shapes, you can specify different distances for the horizontal and the vertical parts of the rounded corners.





