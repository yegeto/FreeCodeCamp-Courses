# Photo Gallery         FreeCodeCamp.org

This repository was created for the "Learn CSS Flexbox by Building a Photo Gallery " course on freecodecamp.org.

Course description:
    Flexbox helps you design your webpage so that it looks good on any screen size.
    In this course, you'll use Flexbox to build a responsive photo gallery webpage.

## HTML

## CSS
Step 8: Notice how the blue image border extends beyond the red gallery border. This is due to the way browsers calculate the size of container elements. The 
    box-sizing property is used to set this behavior. By default, the content-box model is used. With this model, when an element has a specific width, that width is calculated based only on the element's content. Padding and border values get added to the total width, so the element grows to accommodate these values. Try setting box-sizing to content-box explicitly, with the global * selector. At this point, you will not see any changes, because you are using the default value.

    * {
        box-sizing: content-box;
    }

Step 9: The border-box sizing model does the opposite of content-box. The total width of the element, including padding and border, will be the explicit width set. The 
    content of the element will shrink to make room for the padding and border.

    * {
        box-sizing: border-box;
    }

Step 15: Flexbox has a main and cross axis. The main axis is defined by the flex-direction property, which has four possible values:
    * row (default): horizontal axis with flex items from left to right
    * row-reverse: horizontal axis with flex items from right to left
    * column: vertical axis with flex items from top to bottom
    * column-reverse: vertical axis with flex items from bottom to top
    Note: The axes and directions will be different depending on the text direction. The values shown are for a left-to-right text direction.

    .gallery {
        display: flex;
        flex-direction: row;
    }


Step 16: The flex-wrap property determines how your flex items behave when the flex container is too small. Setting it to wrap will allow the items to wrap to the next row or column. nowrap (default) will prevent your items from wrapping and shrink them if needed.

    .gallery {
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;
    }

Step 17: The justify-content property determines how the items inside a flex container are positioned along the main axis, affecting their position and the space around them.

    .gallery {
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;
        justify-content: center;
    }

Step 20: Notice how some of your images have become distorted. This is because the images have different aspect ratios. Rather than setting each aspect ratio individually, you can use the object-fit property to determine how images should behave. Give your .gallery img selector the object-fit property and set it to cover. This will tell the image to fill the img container while maintaining aspect ratio, resulting in cropping to fit.

    .gallery img {
        width: 100%;
        max-width: 350px;
        height: 300px;
        object-fit: cover;
    }

Step 21: Your images need some space between them. The gap CSS shorthand property sets the gaps, also known as gutters, between rows and columns. The gap property and its row-gap and column-gap sub-properties provide this functionality for flex, grid, and multi-column layout. You apply the property to the container element. Give your .gallery flex container a gap property with 16px as the value.

    .gallery {
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;
        justify-content: center;
        align-items: center;
        max-width: 1400px;
        margin: 0 auto;
        padding: 20px 10px;
        gap: 16px;
    }

Step 22: Smooth out your images a bit by giving the .gallery img selector a border-radius property with 10px set as the value.

    .gallery img {
        width: 100%;
        max-width: 350px;
        height: 300px;
        object-fit: cover;
        border-radius: 10px;
    }

Step 23: The ::after pseudo-element creates an element that is the last child of the selected element. You can use it to add an empty element after the last image. If you 
    give it the same width as the images it will push the last image to the left when the gallery is in a two-column layout. Right now, it is in the center because you set justify-content: center on the flex container.

    .gallery::after {
        content: "";
        width: 350px;
    }