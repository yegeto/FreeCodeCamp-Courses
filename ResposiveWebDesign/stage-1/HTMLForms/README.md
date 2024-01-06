# registration-form --- freecodecamp.org


This repository created based on "Learn HTML Forms by  Building Registration Form" course on freecodecamp.org

Course description: "You can use HTML forms to collect information from people who visit your webpage. In this course, you'll learn HTML forms by building a sign up page. You'll learn how to control what types of data people can type into your form, and some new CSS tools for styling your page."



Notes I took to identify the topics I learned:

     HTML

Step 8: The vh unit stands for viewport height, and is relative to 1% of the height of the viewport.

Step 12: The method attribute specifies how to send form-data to the URL specified in the action attribute. The form-data can be sent via a GET request as URL parameters (with method="get") or via a POST request as data in the request body (with method="post").
    
Step 16: The rem unit stands for root em, and is relative to the font size of the html element. As label elements are inline by default, they are all displayed side by side on the same line, making their text hard to read. To make them appear on separate lines, add display: block to the label element, and add a margin of 0.5rem 0, to separate them from each other.
    
    label {
         display: block;
         margin: 0.5rem 0;
    }

Step 18: Following accessibility best practices, link the input elements and the label elements together using the for attribute. Use first-name, last-name, email, and new-password as values for the respective id attributes.
     
     <fieldset>
        <label for="first-name">Enter Your First Name: <input id="first-name" /></label>
        <label for="last-name">Enter Your Last Name: <input id="last-name" /></label>
        <label for="email">Enter Your Email: <input id="email" /></label>
        <label for="new-password">Create a New Password: <input id="new-password" /></label>
      </fieldset>

Step 19: Specifying the type attribute of a form element is important for the browser to know what kind of data it should expect. If the type is not specified, the browser will default to text. The email type only allows emails with a @ and a . in the domain. The password type obscures the input, and warns if the site does not use HTTPS.
     
     <label for="email">Enter Your Email: <input id="email" type="email" /></label>

Step 20: The first input element with a type of submit is automatically set to submit its nearest parent form element.
     
     <input type="submit" value="Submit" />

Step 22: Add custom validation to the password input element, by adding a minlength attribute.
     
     <label for="new-password">Create a New Password: <input id="new-password" type="password" minlength="8" required /></label>

Step 23: With type="password" you can use the pattern attribute to define a regular expression that the password must match to be considered valid. Add a pattern attribute to the password input element to require the input match: [a-z0-5]{8,} The above is a regular expression which matches eight or more lowercase letters or the digits 0 to 5. Then, remove the minlength attribute, and try it out.
     
     <label for="new-password">Create a New Password: <input id="new-password" type="password" pattern="[a-z0-5]{8,}" required /></label>

Step 24: For the terms and conditions, add an input with a type of checkbox to the third label element. Make this input element required because users should not sign up without reading the terms and conditions.
     
     <label><input type="checkbox" required /></label>

Step 28: You only want one radio input to be selectable at a time. However, the form does not know the radio inputs are related. To relate the radio inputs, give them the same name attribute with a value of account-type. Now, it is not possible to select both radio inputs at the same time.
     
     <label><input type="radio" name="account-type" /> Personal Account</label>
     <label><input type="radio" name="account-type" /> Business Account</label>

Step 31: Moving on to the final fieldset. What if you wanted to allow a user to upload a profile picture? Well, the input type file allows just that. Add a label with the text Upload a profile picture: , and nest an input accepting a file upload.
     
     <label><input type="file" />Upload a profile picture:</label>

Step 32: Add another label after the first, with the text Input your age (years): . Then, nest an input with the type of number. Next, add a min attribute to the input with a value of 13 because users under the age of 13 should not register. Also, users probably will not be over the age of 120; add a max attribute with a value of 120.
     
     <label>Input your age (years): <input type="number" min="13" max="120" /></label>

Step 33: Adding a dropdown to the form is easy with the select element. The select element is a container for a group of option elements, and the option element acts as a label for each dropdown option. Both elements require closing tags.
     
     <select>
          <option></option>
     </select>

Step 36: Submitting the form with an option selected would not send a useful value to the server. As such, each option needs to be given a value attribute. Without which, the text content of the option will be submitted to the server.
     
     <select>
          <option value="">(select one)</option>
          <option value="1">freeCodeCamp News</option>
          <option value="2">freeCodeCamp YouTube Channel</option>
          <option value="3">freeCodeCamp Forum</option>
          <option value="4">Other</option>
     </select>

Step 37: The textarea element acts like an input element of type text, but comes with the added benefit of being able to receive multi-line text, and an initial number of text rows and columns.
     
     <label>Provide a bio: 
          <textarea></textarea>
     </label>

Step 39: The textarea appears too small. To give it an initial size, you can add the rows and cols attributes.
     
     <label for="bio">Provide a bio:
          <textarea id="bio" rows="3" cols="30"></textarea>
     </label>

Step 40: To give Campers an idea of what to put in their bio, the placeholder attribute is used. The placeholder accepts a text value, which is displayed until the user starts typing.
     
     <textarea id="bio" rows="3" cols="30" placeholder="I like coding on the beach..."></textarea>

Step 41: With form submissions, it is useful, and good practice, to provide each submittable element with a name attribute. This attribute is used to identify the element in the form submission.
     
     <label for="first-name">Enter Your First Name: <input name="first-name" id="first-name" type="text" required /></label>
     <label for="last-name">Enter Your Last Name: <input name="last-name" id="last-name" type="text" required /></label>
     <label for="email">Enter Your Email: <input name="email" id="email" type="email" required /></label>

     CSS

Step 43: Center the h1 and p elements by giving them a margin of 1em auto. Then, align their text in the center as well.
     
     h1, p {
          text-align: center;
          margin: 1em auto;
     }

Step 44: Center the form element, by giving it a margin of 0 auto. Then, fix its size to a maximum width of 500px, and a minimum width of 300px. In between that range, allow it to have a width of 60vw.
     
     form {
          margin: 0 auto;
          max-width: 500px;
          min-width: 300px;
          width: 60vw;
     }

Step 45: During development, it is useful to see the fieldset default borders. However, they make the content appear too separated. Remove the border, and add 2rem of padding only to the top and bottom of each fieldset. Be sure to remove the padding from the left and right.
     
     fieldset {
          border: 0;
          padding: 2rem 0;
     }

Step 47: The border of the last fieldset element looks a little out of place. You can select the last element of a specific type using the last-of-type CSS pseudo-class, like this: p:last-of-type { } That will select the last p element. Create a new selector that targets the last fieldset element and set its border-bottom to none.
     
     fieldset:last-of-type {
          border-bottom: none;
     }

Step 48: It would be nicer to have the label text appear above the form elements. Select all input, textarea, and select elements, and make them take up the full width of their parent elements. Also, add 10px of margin to the top of the selected elements. Set the other margins to 0.
     
     input, textarea, select {
          margin: 10px 0 0 0;
          width: 100%;
     }

Step 50: Select only the .inline elements, and give them width of unset. This will remove the earlier rule which set all the input elements to width: 100%.
     
     .inline {
          width: unset;
     }

Step 52: If you look close enough, you will notice the .inline elements are too high on the line. To combat this, set the vertical-align property to middle.
     
     .inline {
          width: unset;
          margin: 0 0.5em 0 0;
          vertical-align: middle;
     }

Step 53: To make the input and textarea elements blend in with the background theme, set their background-color to #0a0a23. Then, give them a 1px, solid border with a color of #0a0a23.
     
     input, textarea {
          background-color: #0a0a23;
          border: 1px solid #0a0a23;
     }

Step 56: To style the submit button, you can use an attribute selector, which selects an element based on the given attribute value. Here is an example: input[name="password"] The above selects input elements with a name attribute value of password. Now, use the attribute selector to style the submit button with a display of block, and a width of 60%.
     
     input[type="submit"] {
          display: block;
          width: 60%;
     }

Step 57: With a display of block the submit button sits flush against the left edge of its parent. Use the same technique used to center the form to center the submit button.
     
     input[type="submit"] {
          display: block;
          width: 60%;
          margin: 0 auto;
     }

Step 61: Most browsers inject their own default CSS properties and values for different elements. If you look closely, you might be able to notice the file input is smaller than the other text input elements. By default, a padding of 1px 2px is given to input elements you can type in. Using another attribute selector, style the input with a type of file to be the same padding as the other input elements.
     
     input[type="file"] {
          padding: 1px 2px;
     }
