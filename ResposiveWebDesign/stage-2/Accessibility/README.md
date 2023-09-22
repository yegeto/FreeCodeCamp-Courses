# Accessibility Quiz  

This repository was created for the "Learn Accessibility by Building a Quiz" course on freecodecamp.org.

Course description:
  Accessibility is making your webpage easy for all people to use – even people with disabilities. In this course, you'll build a quiz webpage. You'll learn accessibility tools such as keyboard shortcuts, ARIA attributes, and design best practices.


## Notes I took to identify the topics I learned:

### HTML

#### Step 4: 
Another important meta element for accessibility and SEO is the description definition. The value of the content attribute is used by search engines to provide a description of your page.

    <meta name="description" content="quiz"> 

#### Step 15:
To increase the page accessibility, the role attribute can be used to indicate the purpose behind an element on the page to assistive technologies. The role attribute is a part of the Web Accessibility Initiative (WAI), and accepts preset values.

    <section role="region"></section>

#### Step 16:
Every region role requires a label, which helps screen reader users understand the purpose of the region. One method for adding a label is to add a heading element inside the region and then reference it with the aria-labelledby attribute.

Add the following aria-labelledby attributes to the section elements:

  - student-info
  - html-questions
  - css-questions
  
Then, within each section element, nest one h2 element with an id matching the corresponding aria-labelledby attribute. Give each h2 suitable text content.

    <form method="post" action="https://freecodecamp.org/practice-project/accessibility-quiz">
      <section role="region" aria-labelledby="student-info">
        <h2 id="student-info">Student Info</h2>
      </section>
      <section role="region" aria-labelledby="html-questions">
        <h2 id="html-questions">HTML</h2>
      </section>
      <section role="region" aria-labelledby="css-questions">
        <h2 id="css-questions">CSS</h2>
      </section>
    </form>

#### Step 23:
Arguably, D.O.B. is not descriptive enough. This is especially true for visually impaired users. One way to get around such an issue, without having to add visible text to the label, is to add text only a screen reader can read.

Append a span element with a class of sr-only to the current text content of the third label element.

    <label for="birth-date">D.O.B.<span class="sr-only">(Date of Birth)</span></label>

<a href="#step-25">CSS Code</a>

#### Step 43:
Within the address element, add the following:

    freeCodeCamp<br />
    San Francisco<br />
    California<br />
    USA

The br tags will allow each part of the address to be on its own line and are useful for presenting address elements properly.

### CSS

#### Step 8: 
A useful property of an SVG (scalable vector graphics) is that it contains a path attribute which allows the image to be scaled without affecting the resolution of the resultant image.Currently, the img is assuming its default size, which is too large. CSS has a max function which returns the largest of a set of comma-separated values. For example;

    img {
      width: max(250px, 25vw);
    }

In this example, img elements will have a minimum width of 250px. And as the viewport grows, the image will grow accordingly to be 25 percent of the viewport width.


#### Step 17:
Typeface plays an important role in the accessibility of a page. Some fonts are easier to read than others, and this is especially true on low-resolution screens.


#### Step 25:
The .sr-only text is still visible. There is a common pattern to visually hide text for only screen readers to read.

This pattern is to set the following CSS properties:

    .sr-only {
      position: absolute;
      width: 1px;
      height: 1px;
      padding: 0;
      margin: -1px;
      overflow: hidden;
      clip: rect(0, 0, 0, 0);
      white-space: nowrap;
      border: 0;  
    }

#### Step 34:
To prevent unnecessary repetition, target the before pseudo-element of the p element, and give it a content property of "Question #".

    p::before {
      content: "Question #";
    }

#### Step 43:
The br tags will allow each part of the address to be on its own line and are useful for presenting address elements properly.

    freeCodeCamp<br />
    San Francisco<br />
    California<br />
    USA
