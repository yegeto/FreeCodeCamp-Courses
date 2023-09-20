# set-of-colored-markers    freecodecamp.org


This repository was created for the "Learn CSS Colors by Building a set of Colored Markers" course on freecodecamp.org.

Course description:
    "Selecting the correct colors for your webpage can greatly improve the aesthetic appeal to your readers. In this course, you'll build a set of colored markers. You'll learn different ways to set color values and how to pair colors with each other."


Notes I took to identify the topics I learned:

step 12: set height and width property of a div element. as a result you can 
    see the background color of the empty element.

step 15: when the shorthand margin property has two values, it sets
    top and bottom to the first value, and  left and right to the second value.
    {margin: 10px auto;}

step 16: Multiple classes can be added to an element by listing them in 
    the class attribute and separating them with a space. 
    
    <div class="marker one"></div>

step 21: In this project we use RGB(r, g, b) color model. RGB colors begin as 
    black(0, 0, 0).

step 22: Each red, green, and blue value is a number from 0 to 255. 0 means 
    that there's 0% of that color, and is black. 255 means that there's 100% of that color.

    red: rgb(255, 0, 0) green: rgb(0, 255, 0)  blue: rgb(0, 0, 255) white: (255, 255, 255) 

step 24: The green color keyword is actually a darker shade, and is about 
    halfway between black and the maximum value for green.
    
    rgb(0, 127, 0)

step 25: use the shorthand padding property to add 10px of top and 
    bottom padding, and set the left and right padding to 0
    
    {padding: 10px 0px;}

step 28: Secondary colors are the colors you get when you combine primary colors. 
    
    {yellow rgb(255, 255, 0) cyan rgb(0, 255, 255) magenta rgb(255, 0, 255)}

step 31: Tertiary colors are created by combining a primary with a nearby 
    secondary color.
    
    {orange rgb(255, 127, 0); spring green rgb(0, 255, 127); violet rgb(127, 0, 255);
    chartreuse green rgb(127, 255, 0); azure rgb(0, 127, 255); rose rgb(255, 0, 127);}

step 35: The rgb function uses the additive color model. We can adjust the values
    by subtraction and addition.
    
    {rgb(255, 255, 255) + rgb(-255, -255, -255) = black}

step 36: A color wheel is a circle where similar colors, or hues, are near 
    each other, and different ones are further apart.Two colors that are 
    opposite from each other on the color wheel are called complementary colors.
    If two complementary colors are combined, they produce gray. But when 
    they are placed side-by-side, these colors produce strong visual contrast 
    and appear brighter.

step 46:Hex color values start with a # character and take six characters 
    from 0-9 and A-F. The first pair of characters represent red, the second 
    pair represent green, and the third pair represent blue.
    
    {green #00FF00;}

step 48: The HSL color model, or hue, saturation, and lightness, is another way to 
    represent colors.The CSS hsl function accepts 3 values: a number from 0 to 
    360 for hue, a percentage from 0 to 100 for saturation, and a percentage from 
    0 to 100 for lightness.If you imagine a color wheel, the hue red is at 0 degrees, 
    green is at 120 degrees, and blue is at 240 degrees.Saturation is the intensity 
    of a color from 0 percent, or gray, to 100percent for pure color. You must add 
    the percent sign to the saturation and lightness values.Lightness is how bright 
    a color appears, from 0 percent, or complete black, to 100, complete white, 
    with 50percent  being neutral.
    
    {blue hsl(240 100% 50%);}

step 49: A gradient is when one color transitions into another. The CSS 
    linear-gradient function lets you control the direction of the transition 
    along a line, and which colors are used. One thing to remember is that 
    the linear-gradient function actually creates an image element, and is 
    usually paired with the background property which can accept an image 
    as a value. gradientDirection is the direction of the line used for 
    the transition. color1 and color2 are color arguments, which are 
    the colors that will be used in the transition itself. These can be 
    any type of color, including color keywords, hex, rgb, or hsl.
    
    {red-to-green gradient linear-gradient(90deg, rgb(255, 0, 0), rgb(0, 255, 0));}

step 54: Color-stops allow you to fine-tune where colors are placed along 
    the gradient line. They are a length unit like px or percentages that follow 
    a color in the linear-gradient function. For example, in this red-black gradient, 
    the transition from red to black takes place at the 90% point along the gradient 
    line, so red takes up most of the available space:
    
    {linear-gradient(90deg, red 90%, black);}
    {linear-gradient(rgb(122, 74, 14), rgb(245, 62, 113), rgb(162, 27, 27));}
    {linear-gradient(#55680D, #71F53E, #116C31);}
    {linear-gradient(hsl(186, 76%, 16%), hsl(223, 90%, 60%), hsl(240, 56%, 42%));}

step 73: Opacity describes how opaque, or non-transparent, something is. 
    For example, a solid wall is opaque, and no light can pass through. 
    But a drinking glass is much more transparent, and you can see through 
    the glass to the other side. With the CSS opacity property, you can control 
    how opaque or transparent an element is. With the value 0, or 0%, the 
    element will be completely transparent, and at 1.0, or 100%, the element 
    will be completely opaque like it is by default.

step 75: You're already familiar with using the rgb function to set colors. 
    To add an alpha channel to an rgb color, use the rgba function instead.
    The rgba function works just like the rgb function, but takes one more 
    number from 0 to 1.0 for the alpha channel:
    
    {rgba(redValue, greenValue, blueValue, alphaValue);}

step 78: The default display property for div elements is block. So when 
    two block elements are next to each other, they stack like actual blocks.
    For example, your marker elements are all stacked on top of each other. 
    To position two div elements on the same line, set their display 
    properties to inline-block.

step 79: All HTML elements have borders, though they're usually set to none 
    by default. With CSS, you can control all aspects of an element's border, 
    and set the border on all sides, or just one side at a time. For a border 
    to be visible, you need to set its width and style. Borders have several 
    styles to choose from. You can make your border a solid line, but you can 
    also use a dashed or dotted line if you prefer. Solid border lines are 
    probably the most common.
    
    {border-left-width: 10px; border-left-style: solid; border-left-color: black;}

step 82: The border-left shorthand property lets you to set the left border's 
    width, style, and color at the same time.
    
    {border-left: width style color;}

step 86: The box-shadow property lets you apply one or more shadows around an 
    element. Here's how the offsetX and offsetY values work: both offsetX and 
    offsetY accept number values in px and other CSS units a positive offsetX 
    value moves the shadow right and a negative value moves it left a positive 
    offsetY value moves the shadow down and a negative value moves it up if 
    you want a value of zero (0) for any or both offsetX and offsetY, you don't 
    need to add a unit. Every browser understands that zero means no change. 
    The height and width of the shadow is determined by the height and width of 
    the element it's applied to. You can also use an optional spreadRadius value
    to spread out the reach of the shadow.
    
    {box-shadow: offsetX offsetY blurRadius spreadRadius color;}
    {box-shadow: 0 0 20px 0 rgba(83, 14, 14, 0.8);}
    {box-shadow: 0 0 20px 0 #3B7E20CC;}
    {box-shadow: 0 0 20px 0 hsla(223, 59%, 31%, 0.8);}
    



