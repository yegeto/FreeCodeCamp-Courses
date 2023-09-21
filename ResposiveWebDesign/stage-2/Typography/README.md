# Nutrition Label         FreeCodeCamp.org

This repository was created for the "Learn Typography by Building a Nutrition Label" course on freecodecamp.org.

Course description:
  Typography is the art of styling your text to be easily readable and suit its purpose.In this course, you'll use typography to build a nutrition label webpage. You'll learn how to style text, adjust line height, and position your text using CSS.

## HTML

## CSS

Step 11: If you inspect your .label element with your browser's developer tools, you may notice that it's actually 288 pixels wide instead of 270. This is because, 
by default, the browser includes the border and padding when determining an element's size.To solve this, reset the box model by creating a * selector and giving it a box-sizing property of border-box.

  * {
    box-sizing: border-box;
  }

Step 18: The letter-spacing property can be used to adjust the space between each character of text in an element.

  h1 {
    letter-spacing: 0.15px;
  }

Step 23: Now we can add the horizontal spacing using flex. In your p selector, add a display property set to flex and a justify-content property set to space-between.

  p {
    display: flex;
    justify-content: space-between;
  }

Step 49: The :not pseudo-selector can be used to select all elements that do not match the given CSS rule.

  div:not(#example) {
    color: red;
  }

  .daily-value p:not(.no-divider) {
    border-bottom: 1px  solid #888989;
  }