# Building skyline

## 1. Tags

- Welcome to the CSS Variables Skyline project! Start by adding the !DOCTYPE html declaration at the top of the document so the browser knows what type of document it's reading.

```html
<!DOCTYPE html>
```

## 2

- Add opening and closing html tags below the DOCTYPE so you have a place to start putting some code. Be sure to set the language to English.

```html
<!DOCTYPE html>
<html lang="en">
  </html>
```

## 3

- Next, add opening and closing head and body tags within the html element.

```html
<!DOCTYPE html>
<html lang="en">
<head></head>
<body>
  </body>
</html>
```

## 4

- Within the head, nest a meta element with a charset of UTF-8, a title element with a title of City Skyline, and a link element that links your styles.css file.

```html

<head>
    <title>City Skyline</title>
    <meta charset="utf-8">
    <link rel="stylesheet" href="styles.css">
  </head>
```

## 5

- In CSS, you can target everything with an asterisk. Add a border to everything by using the * selector, and giving it a border of 1px solid black. This is a trick that helps visualize where elements are and their size. You will remove this later.

```html
* {
  border: 1px solid black;
}
```

## 6

- Also add a box-sizing of border-box to everything. This will make it so the border you added doesn't add any size to your elements.

```html
* {
  border: 1px solid black;
  box-sizing: border-box;
}
```

## 7

- You can see the body (it's the inner-most box on your page); the box around it is the html element. Make your body fill the whole viewport by giving it a height of 100vh. Remove the default margin from the body by setting the margin to 0. Finally, set the overflow property to hidden to hide any scroll bars that appear when something extends past the viewport.

```html
body {
  height: 100vh;
  margin: 0;
  overflow: hidden;
}

```

## 8

- Create a div element in the body with a class of background-buildings. This will be a container for a group of buildings.

```html
<body>
    <div class="background-buildings"></div>
  </body>
```

## 9

- Give your .background-buildings element a width and height of 100% to make it the full width and height of its parent, the body.

```html
.background-buildings {
  width: 100%;
  height: 100%;
}
```

## 10

- Nest a div with a class of bb1 in the background buildings container. Open your styles.css file, and give .bb1 a width of 10% and height of 70%. "bb" stands for "background building", this will be your first building.

```html
<div class="background-buildings">
      <div class="bb1">
        </div>
    </div>
```

## 11

- Nest four div elements in the .bb1 container. Give them the classes bb1a, bb1b, bb1c, and bb1d in that order. This building will have four sections.

```html

<div class="bb1">
        <div class="bb1a"></div>
        <div class="bb1b"></div>
        <div class="bb1c"></div>
        <div class="bb1d"></div>
      </div>

```

## 12

- Give the parts of your building width and height properties with these values: 70% and 10% to .bb1a, 80% and 10% to .bb1b, 90% and 10% to .bb1c, and 100% and 70% to .bb1d. Remember that these percentages are relative to the parent and note that the heights will add up to 100% - vertically filling the container.

```html
.bb1a {
  width: 70%;
  height: 10%;
}

.bb1b {
  width: 80%;
  height: 10%;
}

.bb1c {
  width: 90%;
  height: 10%;
}

.bb1d {
  width: 100%;
  height: 70%;
}
```

## 13

- Center the parts of your building by turning the .bb1 element into a flexbox parent. Use the flex-direction and align-items properties to center the children.

```html
.bb1 {
  width: 10%;
  height: 70%;
  flex-direction: column;
  display: flex;
  align-items: center;
}
```

## 14

- Now you have something that is resembling a building. You are ready to create your first variable. Variable declarations begin with two dashes (-) and are given a name and a value like this: --variable-name: value;. In the rule for the bb1 class, create a variable named --building-color1 and give it a value of #999.

```html
.bb1 {
  width: 10%;
  height: 70%;
  display: flex;
  flex-direction: column;
  align-items: center;
  --building-color1:#999;
}
```

## 15

- To use a variable, put the variable name in parentheses with var in front of them like this: var(--variable-name). Whatever value you gave the variable will be applied to whatever property you use it on.

- Add the variable --building-color1 you created in the previous step as the value of the background-color property of the .bb1a class.

```html
.bb1a {
  width: 70%;
  height: 10%;
  background-color: var(--building-color1);
}
```

## 16

- Use the same variable as the background-color of the .bb1b, .bb1c, and .bb1d classes to fill in the rest of the building.

```html
 .bb1b {
  width: 80%;
  height: 10%;
  background-color: var(--building-color1);
}

.bb1c {
  width: 90%;
  height: 10%;
  background-color: var(--building-color1);
}

.bb1d {
  width: 100%;
  height: 70%;
  background-color: var(--building-color1);
}
```

## 17

- Change the value of your variable from #999 to #aa80ff and you can see how it gets applied everywhere you used the variable. This is the main advantage of using variables, being able to quickly change many values in your stylesheet by just changing the value of a variable.

```html
--building-color1: #aa80ff;
```

## 18

- Your first building looks pretty good now. Nest three new div elements in the .background-buildings container and give them the classes of bb2, bb3, and bb4 in that order. These will be three more buildings for the background.

```html
 <div class="bb2"></div>
<div class="bb3"></div>
<div class="bb4"></div>
```

## 19

- Give the new buildings width and height properties of: 10% and 50% for .bb2, 10% and 55% for .bb3, and 11% and 58% for .bb4. You will be using almost all percent based units and some flexbox for this project, so everything will be completely responsive.

```html
.bb2 {
  width: 10%;
  height: 50%;
}

.bb3 {
  width: 10%;
  height: 55%;
}

.bb4 {
  width: 11%;
  height: 58%;
}
```

## 20

- The buildings are currently stacked on top of each other. Align the buildings by turning the .background-buildings element into a flexbox parent. Use the align-items and justify-content properties to evenly space the buildings across the bottom of the element.

```html
.background-buildings {
  width: 100%;
  height: 100%;
  display: flex;
  align-items: flex-end;
  justify-content: space-evenly;
}
 ```

## 21

- At this point, you should be able to submit the form. However, you might notice not much happens.

- To make the form more interactive, add the required attribute to the input elements in the first fieldset.

- Now, if you try to submit the form without filling in the required fields, you will see an error message.

```html
<fieldset>
        <label for="first-name">Enter Your First Name: <input id="first-name" type="text" required="" /></label>
        <label for="last-name">Enter Your Last Name: <input id="last-name" type="text" required="" /></label>
        <label for="email">Enter Your Email: <input id="email" type="email" required="" /></label>
        <label for="new-password">Create a New Password: <input id="new-password" type="password" required="" /></label>
      </fieldset>
      <fieldset></fieldset>
      <fieldset></fieldset>
      <input type="submit" value="Submit" />
 ```

## 22

- Certain type attribute values come with built-in form validation. For example, type="email" requires that the value be a valid email address.

- Add custom validation to the password input element, by adding a minlength attribute with a value of 8. Doing so prevents inputs of less than 8 characters being submitted.

```html
<fieldset>
        <label for="first-name">Enter Your First Name: <input id="first-name" type="text" required /></label>
        <label for="last-name">Enter Your Last Name: <input id="last-name" type="text" required /></label>
        <label for="email">Enter Your Email: <input id="email" type="email" required /></label>
        <label for="new-password">Create a New Password: <input id="new-password" type="password" required minlength="8" /></label>
      </fieldset>
 ```

## 23

- With type="password" you can use the pattern attribute to define a regular expression that the password must match to be considered valid.

- Add a pattern attribute to the password input element to require the input match: [a-z0-5]{8,}

- The above is a regular expression which matches eight or more lowercase letters or the digits 0 to 5. Then, remove the minlength attribute, and try it out.

```html
<fieldset>
        <label for="first-name">Enter Your First Name: <input id="first-name" type="text" required /></label>
        <label for="last-name">Enter Your Last Name: <input id="last-name" type="text" required /></label>
        <label for="email">Enter Your Email: <input id="email" type="email" required /></label>
        <label for="new-password">Create a New Password: <input id="new-password" type="password"  pattern="[a-z0-5]{8,}" required  /></label>
      </fieldset>
 ```

## 24

- Let us go to the next part of the registration form. This section will ask for the type of account the user is opening.

- Start by adding two label elements to the second fieldset.

```html
<fieldset>
        <label></label>
        <label></label>
      </fieldset>
 ```

## 25

- Users will be allowed to choose either a Personal or Business.

- To do this, within each of the first two label elements, add one input element with type="radio".

```html
<fieldset>
        <label> <input type="radio" /></label>
        <label> <input type="radio" /></label>
      </fieldset>
 ```

## 26

- Within each corresponding label element, and immediately after the input element, add a space and add the following text:

Example Code
Personal
Business

```html
<label><input type="radio" /> Personal</label>
        <label><input type="radio" /> Business</label>
 ```

## 27

- You only want one radio input to be selectable at a time. However, the form does not know the radio inputs are related.

- To relate the radio inputs, give them the same name attribute with a value of account-type. Now, it is not possible to select both radio inputs at the same time.

```html
  <fieldset>
        <label><input type="radio" name="account-type" /> Personal</label>
        <label><input type="radio" name="account-type" /> Business</label>
      </fieldset>
 ```

## 28

- Currently users can submit the form without checking the radio inputs. Although you previously used the required attribute to indicate that an input is required, it won't work in this case because adding required to both inputs will convey the wrong information to users.

- To solve this, you can provide context of what is needed by adding a legend element with text Account type (required) before the label elements within the second fieldset. Then add the checked attribute to the Personal input to ensure the form is submitted with the required data in it.

```html
<fieldset>
        <legend>Account type (required)</legend>
        <label><input type="radio" name="account-type" checked /> Personal</label>
        <label><input type="radio" name="account-type" /> Business</label>
      </fieldset>
```

## 29

- Follow accessibility best practices by linking the input elements and the label elements in the second fieldset.

- Use personal-account, and business-account as values for the respective id attributes.

```html
<fieldset>
        <legend>Account type (required)</legend>
        <label for="personal-account"><input type="radio" name="account-type" id="personal-account" checked /> Personal</label>
        <label for="business-account"><input type="radio" name="account-type" id="business-account" /> Business</label>
      </fieldset>
```

## 30

- You need to confirm that the user has read the terms and conditions.

- Add a label element. Inside the newly created label element add an input element and set the type attribute to checkbox. Make this input element required so users can not sign up without agreeing to the terms and conditions.

- Add an id and for attribute with the value terms-and-conditions to the elements for accessibility.

```html
<label for="terms-and-conditions">
  <input type="checkbox" required id="terms-and-conditions" />
  </label>
```

## 31

- Add the text I accept the terms and conditions immediately after the input element in the newly added label. Then link the text terms and conditions to the following location:

Example Code
<!--  https://www.freecodecamp.org/news/terms-of-service/ -->

```html
<label for="terms-and-conditions"><input id="terms-and-conditions" type="checkbox" required />I accept the <a href="https://www.freecodecamp.org/news/terms-of-service/">terms and conditions</a></label>
```

## 32

- Moving on to the final fieldset. What if you wanted to allow a user to upload a profile picture?

- Well, the input type file allows just that. Add a label with the text Upload a profile picture: , and nest an input accepting a file upload.

```html
<fieldset>
        <label> <input type="file" />Upload a profile picture: </label>
      </fieldset>
```

## 33

- Add another label after the first, with the text Input your age (years): . Then, nest an input with the type of number.

- Next, add a min attribute to the input with a value of 13 because users under the age of 13 should not register. Also, users probably will not be over the age of 120; add a max attribute with a value of 120.

- Now, if someone tries to submit the form with values outside of the range, a warning will appear, and the form will not submit. Give it a try.

```html
<fieldset>
        <label>Upload a profile picture: <input type="file" /></label>
        <label> Input your age (years): <input type="number" min="13" max="120" /></label>
        
      </fieldset>
```

## 34

- Adding a dropdown to the form is easy with the select element. The select element is a container for a group of option elements, and the option element acts as a label for each dropdown option. Both elements require closing tags.

- Start by adding a select element below the two label elements. Then nest 5 option elements within the select element.

```html
 <fieldset>
        <label>Upload a profile picture: <input type="file" /></label>
        <label>Input your age (years): <input type="number" min="13" max="120" /></label>
        <select>
          <option> </option>
          <option> </option>
          <option> </option>
          <option> </option>
          <option> </option>
          </select>
      </fieldset>
```

## 35

- Nest the select element (with its option elements) within a label element with the text How did you hear about us?. The text should come before the select element.

```html
<fieldset>
        <label>Upload a profile picture: <input type="file" /></label>
        <label>Input your age (years): <input type="number" min="13" max="120" /></label>
        <label>How did you hear about us?<select></label>
          <option></option>
          <option></option>
          <option></option>
          <option></option>
          <option></option>
        </select>
      </fieldset>
```

## 36

- The dropdown options are currently empty. To give them content, add the following text to each subsequent option element:

Example Code
(select one)
freeCodeCamp News
freeCodeCamp YouTube Channel
freeCodeCamp Forum
Other

```html
<fieldset>
        <label>Upload a profile picture: <input type="file" /></label>
        <label>Input your age (years): <input type="number" min="13" max="120" /></label>
        <label>How did you hear about us?
          <select>
            <option>(select one)</option>
            <option>freeCodeCamp News</option>
            <option>freeCodeCamp YouTube Channel</option>
            <option>freeCodeCamp Forum</option>
            <option>Other</option>
          </select>
        </label>
      </fieldset>
```

## 37

- Submitting the form with an option selected would not send a useful value to the server. As such, each option needs to be given a value attribute. Without which, the text content of the option will be submitted to the server.

- Give the first option a value of "", and the subsequent option elements value attributes from 1 to 4.

```html
<fieldset>
        <label>Upload a profile picture: <input type="file" /></label>
        <label>Input your age (years): <input type="number" min="13" max="120" /></label>
        <label>How did you hear about us?
          <select>
            <option value="">(select one)</option>
            <option value="1">freeCodeCamp News</option>
            <option value="2">freeCodeCamp YouTube Channel</option>
            <option value="3">freeCodeCamp Forum</option>
            <option value="4">Other</option>
          </select>
        </label>
      </fieldset>
```

## 38

- The textarea element acts like an input element of type text, but comes with the added benefit of being able to receive multi-line text, and an initial number of text rows and columns.

- Users will be able to register with a bio. Add a label with the text Provide a bio: at the end of the fieldset. Add a textarea element inside the label element. Note that the textarea requires a closing tag.

```html
<fieldset>
        <label>Upload a profile picture: <input type="file" /></label>
        <label>Input your age (years): <input type="number" min="13" max="120" /></label>
        <label>How did you hear about us?
          <select>
            <option value="">(select one)</option>
            <option value="1">freeCodeCamp News</option>
            <option value="2">freeCodeCamp YouTube Channel</option>
            <option value="3">freeCodeCamp Forum</option>
            <option value="4">Other</option>
          </select>
        </label>
        <label>Provide a bio:
          <textarea></textarea></label>
      </fieldset>
```

## 39

- Link the applicable form elements and their label elements together.

- Use profile-picture, age, referrer, and bio as values for the respective id attributes.

```html
<fieldset>
        <label for="profile-picture">Upload a profile picture: <input type="file" id="profile-picture" /></label>
        <label for="age">Input your age (years): <input type="number" min="13" max="120" id="age" /></label>
        <label for="referrer">How did you hear about us?
          <select id="referrer">
            <option value="">(select one)</option>
            <option value="1">freeCodeCamp News</option>
            <option value="2">freeCodeCamp YouTube Channel</option>
            <option value="3">freeCodeCamp Forum</option>
            <option value="4">Other</option>
          </select>
        </label>
        <label for="bio">Provide a bio:
          <textarea id="bio"></textarea>
        </label>
      </fieldset>
```

## 40

- The textarea appears too small. To give it an initial size, you can add the rows and cols attributes.

- Add an initial size of 3 rows and 30 columns.

```html
<fieldset>
        <label for="profile-picture">Upload a profile picture: <input id="profile-picture" type="file" /></label>
        <label for="age">Input your age (years): <input id="age" type="number" min="13" max="120" /></label>
        <label for="referrer">How did you hear about us?
          <select id="referrer">
            <option value="">(select one)</option>
            <option value="1">freeCodeCamp News</option>
            <option value="2">freeCodeCamp YouTube Channel</option>
            <option value="3">freeCodeCamp Forum</option>
            <option value="4">Other</option>
          </select>
        </label>
        <label for="bio">Provide a bio:
          <textarea id="bio" rows="3" cols="30"></textarea>
        </label>
      </fieldset>
```

## 41

- To give Campers an idea of what to put in their bio, the placeholder attribute is used. The placeholder accepts a text value, which is displayed until the user starts typing.

- Give the textarea a placeholder of I like coding on the beach....

```html
<fieldset>
        <label for="profile-picture">Upload a profile picture: <input id="profile-picture" type="file" /></label>
        <label for="age">Input your age (years): <input id="age" type="number" min="13" max="120" /></label>
        <label for="referrer">How did you hear about us?
          <select id="referrer">
            <option value="">(select one)</option>
            <option value="1">freeCodeCamp News</option>
            <option value="2">freeCodeCamp YouTube Channel</option>
            <option value="3">freeCodeCamp Forum</option>
            <option value="4">Other</option>
          </select>
        </label>
        <label for="bio">Provide a bio:
          <textarea id="bio" rows="3" cols="30" placeholder="I like coding on the beach..."></textarea>
        </label>
      </fieldset>

```

## 42

- With form submissions, it is useful, and good practice, to provide each submittable element with a name attribute. This attribute is used to identify the element in the form submission.

- Except for the two radio inputs (which you have already named), give each submittable element a unique name attribute of your choosing.

```html
<fieldset>
        <label for="first-name">Enter Your First Name: <input id="first-name" type="text"  required name="first-name" /></label>
        <label for="last-name">Enter Your Last Name: <input id="last-name" type="text" required name="last-name" /></label>
        <label for="email">Enter Your Email: <input id="email" type="email" required name="email" /></label>
        <label for="new-password">Create a New Password: <input id="new-password" type="password" pattern="[a-z0-5]{8,}" required name="password" /></label>
      </fieldset>
      <fieldset>
        <legend>Account type (required)</legend>
        <label for="personal-account"><input id="personal-account" type="radio" name="account-type" checked /> Personal</label>
        <label for="business-account"><input id="business-account" type="radio" name="account-type" /> Business</label>
      </fieldset>
      <fieldset>
        <label for="profile-picture">Upload a profile picture: <input id="profile-picture" type="file" name="profile-picture" /></label>
        <label for="age">Input your age (years): <input id="age" type="number" min="13" max="120" name="age" /></label>
        <label for="referrer">How did you hear about us?
          <select id="referrer" name="referrer">
            <option value="">(select one)</option>
            <option value="1">freeCodeCamp News</option>
            <option value="2">freeCodeCamp YouTube Channel</option>
            <option value="3">freeCodeCamp Forum</option>
            <option value="4">Other</option>
          </select>
        </label>
        <label for="bio">Provide a bio:
          <textarea id ="bio" rows="3" cols="30" placeholder="I like coding on the beach..." name="bio"></textarea>
        </label>
      </fieldset>
      <label for="terms-and-conditions">
        <input id="terms-and-conditions" type="checkbox" required name="terms" /> I accept the <a href="https://www.freecodecamp.org/news/terms-of-service/">terms and conditions</a>
      </label>
```

## 43

- The HTML for the registration form is finished. Now, you can spruce it up a bit.

- Start by changing the font to Tahoma, and the font size to 16px in the body.

```html
body {
  width: 100%;
  height: 100vh;
  margin: 0;
  background-color: #1b1b32;
  color: #f5f6f7;
  font-family: Tahoma;
  font-size: 16px
}
```

## 44

- Center the h1 and p elements by giving them a margin of 1em auto. Then, align their text in the center as well.

```html
h1, p {
  margin: 1em auto;
  text-align: center;
}
```

## 45

- Center the form element, by giving it a margin of 0 auto. Then, fix its size to a maximum width of 500px, and a minimum width of 300px. In between that range, allow it to have a width of 60vw.

```html
form {
  margin: 0 auto;
  min-width: 300px;
  width: 60vw;
  max-width: 500px;
}

```

## 46

- During development, it is useful to see the fieldset default borders. However, they make the content appear too separated.

- Remove the border, and add 2rem of padding only to the top and bottom of each fieldset. Be sure to remove the padding from the left and right.

```html
fieldset {
  border: 0;
  padding-left:0;
  padding-right:0;
  padding-top:2rem;
  padding-bottom:2rem;
}
```

## 47

- To give the fieldset elements a bit of separation, select them and give them a border-bottom of 3px solid #3b3b4f.

```html
fieldset {
  border: none;
  padding: 2rem 0;
  border-bottom: 3px solid #3b3b4f;
}
```

## 48

- The border of the last fieldset element looks a little out of place. You can select the last element of a specific type using the last-of-type CSS pseudo-class, like this:

Example Code
p:last-of-type { }
That will select the last p element. Create a new selector that targets the last fieldset element and set its border-bottom to none.

```html
fieldset:last-of-type {
  border-bottom: none;
 }

```

## 49

- It would be nicer to have the label text appear above the form elements.

- Select all input, textarea, and select elements, and make them take up the full width of their parent elements.

- Also, add 10px of margin to the top of the selected elements. Set the other margins to 0.

```html

input, textarea, select {
  width:100%;
  margin-bottom: 0;
  margin-top: 10px;
  margin-left: 0;
  margin-right: 0;
}

```

## 50

- For the second fieldset, you want the input and label text to appear on the same line.

- Start, by giving the input elements in the second fieldset a class of inline.

```html

<fieldset>
        <legend>Account type (required)</legend>
        <label for="personal-account"><input id="personal-account" type="radio" name="account-type" class="inline" checked /> Personal</label>
        <label for="business-account"><input id="business-account" type="radio" name="account-type" class="inline" /> Business</label>
      </fieldset>

          
```

## 51

- Select only the .inline elements, and give them width of unset. This will remove the earlier rule which set all the input elements to width: 100%.

```html

.inline {
  width: unset;
}

          
```

## 52

- Add some space between the .inline elements and the label text, by giving a right margin of 0.5em. Also, set all the other margin to 0.

```html

.inline {
  width: unset;
  margin-right: 0.5em;
  margin-left: 0;
  margin-top: 0;
  margin-bottom: 0;

}
          
```

## 53

- If you look close enough, you will notice the .inline elements are too high on the line.

- To combat this, set the vertical-align property to middle.

```html

.inline {
  width: unset;
  margin: 0 0.5em 0 0;
  vertical-align: middle;
}

```

## 54

- To make the input and textarea elements blend in with the background theme, set their background-color to #0a0a23. Then, give them a 1px, solid border with a color of #0a0a23.

```html

input, textarea {
  background-color: #0a0a23;
  border: 1px solid #0a0a23;
}
```

## 55

- Currently, if you type in the input or textarea elements, you will not be able to see the text. Also, their height is too small to be easy to use.

- Fix this, by setting the color to #ffffff, and setting their min-height to 2em.

```html

input, textarea {
  background-color: #0a0a23;
  border: 1px solid #0a0a23;
  color: #ffffff;
  min-height: 2em;
}

```

## 56

- You want the select element to remain with a white background, but now it is not getting the same min-height as the input and textarea elements.

- Move the min-height property and value so that all three element types have the same min-height value, and the select element still has a white background.

```html

body {
  width: 100%;
  height: 100vh;
  margin: 0;
  background-color: #1b1b32;
  color: #f5f6f7;
  font-family: Tahoma;
  font-size: 16px;
}

h1, p {
  margin: 1em auto;
  text-align: center;
}

form {
  width: 60vw;
  max-width: 500px;
  min-width: 300px;
  margin: 0 auto;
}

fieldset {
  border: none;
  padding: 2rem 0;
  border-bottom: 3px solid #3b3b4f;
}

fieldset:last-of-type {
  border-bottom: none;
}

label {
  display: block;
  margin: 0.5rem 0;
}

input,
textarea,
select {
  margin: 10px 0 0 0;
  width: 100%;
  min-height: 2em;
}

input, textarea {
  background-color: #0a0a23;
  border: 1px solid #0a0a23;
  color: #ffffff;
}

.inline {
  width: unset;
  margin: 0 0.5em 0 0;
  vertical-align: middle;
}


```

## 57

- To style the submit button, you can use an attribute selector, which selects an element based on the given attribute value. Here is an example:

Example Code
input[name="password"]
The above selects input elements with a name attribute value of password.

- Now, use the attribute selector to style the submit button with a display of block, and a width of 60%.

```html

input[type="submit"] {
  display: block;
  width: 60%;
}

```

## 58

- With a display of block the submit button sits flush against the left edge of its parent.

- Use the same technique used to center the form to center the submit button.

```html

input[type="submit"] {
  display: block;
  width: 60%;
  margin: 0 auto;
}

```

## 59

- To make the submit button look more in line with the rest of the form, give it the same height as the other fields (2em). Also, increase the font-size to 1.1rem.

```html

input[type="submit"] {
  display: block;
  width: 60%;
  margin: 0 auto;
  height: 2em;
  font-size: 1.1rem;
}
 ```

## 60

- To make the submit button appear more distinct, give it a background-color of #3b3b4f, and a border-color of white.

```html

input[type="submit"] {
  display: block;
  width: 60%;
  margin: 0 auto;
  height: 2em;
  font-size: 1.1rem;
  background-color:#3b3b4f;
  border-color: white;
}
 ```

## 61

- Lastly, for the submit button, you want to separate it from the fieldset above, and adjust its width to never be below 300px.

- Change the margin property to include 1em on the top and bottom, while leaving the right and left margins set to auto. Then set the width as described above.

```html

input[type="submit"] {
  display: block;
  width: 60%;
  margin: 0 auto;
  height: 2em;
  font-size: 1.1rem;
  background-color: #3b3b4f;
  border-color: white;
  margin-top: 1em;
  margin-bottom: 1em;
  min-width: 300px;
}

 ```

## 62

- Most browsers inject their own default CSS properties and values for different elements. If you look closely, you might be able to notice the file input is smaller than the other text input elements. By default, a padding of 1px 2px is given to input elements you can type in.

- Using another attribute selector, style the input with a type of file to be the same padding as the other input elements.

```html

input[type="file"] {
  padding: 1px 2px;
}
```

## 63

- Speaking of padding, the submit button is sitting at the bottom of the form element. Add 2em of padding only to the bottom of the form.

```html

form {
  width: 60vw;
  max-width: 500px;
  min-width: 300px;
  margin: 0 auto;
  padding: 2em;
}
```

## 64

- Make the input for the terms and conditions inline by adding the appropriate class in the HTML.

```html

<label for="terms-and-conditions">
        <input id="terms-and-conditions" type="checkbox" required name="terms-and-conditions" class="inline" /> I accept the <a href="https://www.freecodecamp.org/news/terms-of-service/">terms and conditions</a>
      </label>
```

## 65

- Lastly change the text color of the terms and conditions link element to #dfdfe2 by adding a new selector in the CSS.

- Well done! You have completed the final part of the Registration Form practice project.

```html
a {
  color: #dfdfe2;
}
```

## 66

- Now you'll apply a gradient to the blue marker, this time using the hsl function as color arguments.

- In the .blue CSS rule, change the background-color property to background.

```html
.blue {
  background: hsl(240, 100%, 50%);
}
```
