# Accessibility Quiz   FreeCodeCamp.org

This repository was created for the "Learn Accessibility by Building a Quiz" course on freecodecamp.org.

Course description:
  Accessibility is making your webpage easy for all people to use – even people with disabilities. In this course, you'll build a quiz webpage. You'll learn accessibility tools such as keyboard shortcuts, ARIA attributes, and design best practices.

## HTML

Step 4: Another important meta element for accessibility and SEO is the description definition. The value of the content attribute is used by search engines to provide a description of your page.

    <meta name="description" content="quiz">  

## CSS

Step 8: A useful property of an SVG (scalable vector graphics) is that it contains a path attribute which allows the image to be scaled without affecting the resolution of the resultant image.Currently, the img is assuming its default size, which is too large. CSS has a max function which returns the largest of a set of comma-separated values. In this example, img elements will have a minimum width of 250px. And as the viewport grows, the image will grow accordingly to be 25 percent of the viewport width.

    img {
      width: max(250px, 25vw);
    }
