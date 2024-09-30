# Building Quiz

## 1. Tags

- Welcome to the first part of the Accessibility Quiz. As you are becoming a seasoned HTML and CSS developer, we have started you off with the basic boilerplate.

- Start this accessibility journey by providing a lang attribute to your html element. This will assist screen readers in identifying the language of the page.

```html
<html lang="en">
  <head>
    <link rel="stylesheet" href="styles.css" />
  </head>
  <body>

  </body>
</html>
```

## 2

- You may be familiar with the meta element already; it is used to specify information about the page, such as the title, description, keywords, and author.

- Give your page a meta element with an appropriate charset value.

- The charset attribute specifies the character encoding of the page, and, nowadays, UTF-8 is the only encoding supported by most browsers.

```html
<head>
    <link rel="stylesheet" href="styles.css" />
    <meta charset="UTF-8">
  </head>
```

## 3

- Continuing with the meta elements, a viewport definition tells the browser how to render the page. Including one betters visual accessibility on mobile, and improves SEO (search engine optimization).

- Add a viewport definition with a content attribute detailing the width and initial-scale of the page.

```html
<head>
    <meta charset="UTF-8" />
    <link rel="stylesheet" href="styles.css" />
    <meta name="viewport" content="width=device-width, initial-scale=1">
  </head>
```

## 4

- Another important meta element for accessibility and SEO is the description definition. The value of the content attribute is used by search engines to provide a description of your page.

- Add a meta element with the name attribute set to description, and give it a useful content attribute.

```html
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="styles.css" />
    <meta name="description" content="value">
  </head>
```

## 5

- Lastly in the head, the title element is useful for screen readers to understand the content of a page. Furthermore, it is an important part of SEO.

- Give your page a title that is descriptive and concise.

```html
<head>
    <title>Accessibility Quiz</title>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta name="description" content="freeCodeCamp Accessibility Quiz practice project" />
    <link rel="stylesheet" href="styles.css" />
  </head>
```

## 6

- Navigation is a core part of accessibility, and screen readers rely on you to provide the structure of your page. This is accomplished with semantic HTML elements.

- Add a header and a main element to your page.

- The header element will be used to introduce the page, as well as provide a navigation menu.

- The main element will contain the core content of your page.

```html
<body>
    
<header>
    
  </header>
    <main></main>
  </body>
```

## 7

- Within the header, provide context about the page by nesting one img, h1, and nav element.

<!-- The img should point to https://cdn.freecodecamp.org/platform/universal/fcc_primary.svg, have an id of logo, and have an alt text of freeCodeCamp. -->

- The h1 should contain the text HTML/CSS Quiz

```html
<header>
      <img src="https://cdn.freecodecamp.org/platform/universal/fcc_primary.svg" id="logo" alt="freeCodeCamp">
      <h1>HTML/CSS Quiz</h1>
      <nav>
    </header>
```

## 8

- A useful property of an SVG (scalable vector graphics) is that it contains a path attribute which allows the image to be scaled without affecting the resolution of the resultant image.

- Currently, the img is assuming its default size, which is too large. CSS has a max function which returns the largest of a set of comma-separated values. For example:

Example Code
img {
  width: max(250px, 25vw);
}
In the above example, the width of the image will be 250px if the viewport width is less than 1000 pixels. If the viewport width is greater than 1000 pixels, the width of the image will be 25vw. This is because 25vw is equal to 25% of the viewport width.

- Scale the image using its id as a selector, and setting the width to be the maximum of 10rem or 18vw.

```html

#logo {
  width: max(10rem, 18vw);
}
```

## 9

- As described in the freeCodeCamp Style Guide, the logo should retain an aspect ratio of 35 / 4, and have padding around the text.

- First, change the background-color to #0a0a23 so you can see the logo. Then, use the aspect-ratio property to set the desired aspect ratio to 35 / 4. Finally, add a padding of 0.4rem all around.

```html
#logo {
  width: max(10rem, 18vw);
  background-color: #0a0a23;
  aspect-ratio: 35/4;
  padding: 0.4rem;
}
```

## 10

- Make the header take up the full width of its parent container, set its height to 50px, and set the background-color to #1b1b32. Then, set the display to use Flexbox.

```html
header {
  width: 100%;
  height: 50px;
  background-color: #1b1b32;
  display: flex;
}
```

## 11

- Change the h1 font color to #f1be32, and set the font size to min(5vw, 1.2em).

```html

h1 {
  color: #f1be32;
  font-size: min(5vw, 1.2em);
}

```

## 12

- To enable navigation on the page, add an unordered list with the following three list items:

INFO
HTML
CSS
The list items text should be wrapped in anchor tags.

```html
<nav>
        <ul>
          <li><a>INFO</a></li>
          <li><a>HTML</a></li>
          <li><a>CSS</a></li>
            
          </ul>
      </nav>
```

## 13

- The child combinator selector > is used between selectors to target only elements that match the second selector and are a direct child of the first selector.

- This can be helpful when you have deeply nested elements and want to control the scope of your styling.

- Use the > selector to target the unordered list elements within the nav elements, and use Flexbox to evenly space the children.

```html
nav > ul {
    display: flex;
    justify-content: space-evenly;
}
```

## 14

- As this is a quiz, you will need a form for users to submit answers. You can semantically separate the content within the form using section elements.

<!-- Within the main element, create a form with three nested section elements. Then, make the form submit to https://freecodecamp.org/practice-project/accessibility-quiz, using the correct method. -->

```html
<main>
      <form action="https://freecodecamp.org/practice-project/accessibility-quiz" method="post">
      <section></section>
      <section></section>
      <section></section>
    </main>
```

## 15

- To increase the page accessibility, the role attribute can be used to indicate the purpose behind an element on the page to assistive technologies. The role attribute is a part of the Web Accessibility Initiative (WAI), and accepts preset values.

- Give each of the section elements the region role.

```html
<form method="post" action="https://freecodecamp.org/practice-project/accessibility-quiz">
        <section role="region"></section>
        <section role="region"></section>
        <section role="region"></section>
      </form>
```

## 16

- Every region role requires a label, which helps screen reader users understand the purpose of the region. One method for adding a label is to add a heading element inside the region and then reference it with the aria-labelledby attribute.

Add the following aria-labelledby attributes to the section elements:

student-info
html-questions
css-questions
Then, within each section element, nest one h2 element with an id matching the corresponding aria-labelledby attribute. Give each h2 suitable text content.

```html
 <form method="post" action="https://freecodecamp.org/practice-project/accessibility-quiz">
        <section role="region" aria-labelledby="student-info"><h2 id="student-info">Student Info</h2></section>
        <section role="region" aria-labelledby="html-questions"><h2 id="html-questions">html-questions</h2></section>
        <section role="region" aria-labelledby="css-questions"><h2 id="css-questions">css</h2></section>
      </form>
```

## 17

- Typeface plays an important role in the accessibility of a page. Some fonts are easier to read than others, and this is especially true on low-resolution screens.

- Change the font for both the h1 and h2 elements to Verdana, and use another web-safe font in the sans-serif family as a fallback.

- Also, add a border-bottom of 4px solid #dfdfe2 to h2 elements to make the sections distinct.

```html
h1, h2 {
  font-family: Verdana, sans-serif;
}

h2 {
  border-bottom: 4px solid #dfdfe2;
}
```

## 18

- To be able to navigate within the page, give each anchor element an href corresponding to the id of the h2 elements.

```html
<ul>
          <li><a href="#student-info">INFO</a></li>
          <li><a href="#html-questions">HTML</a></li>
          <li><a href="#css-questions">CSS</a></li>
        </ul>
```

## 19

- Filling out the content of the quiz, below #student-info, add three div elements with a class of info.

- Then, within each div nest one label element, and one input element.

```html
<section role="region" aria-labelledby="student-info">
          <h2 id="student-info">Student Info</h2>
          <div class="info"><label></label><input></input></div>
          <div class="info"><label></label><input></input></div>
          <div class="info"><label></label><input></input></div>
        </section>
```

## 20

- It is important to link each input to the corresponding label element. This provides assistive technology users with a visual reference to the input.

- This is done by giving the label a for attribute, which contains the id of the input.

- This section will take a student's name, email address, and date of birth. Give the label elements appropriate for attributes, as well as text content. Then, link the input elements to the corresponding label elements.

```html
<section role="region" aria-labelledby="student-info">
          <h2 id="student-info">Student Info</h2>
          <div class="info">
            <label for="name">Name</label>
            <input id="name" />
          </div>
          <div class="info">
            <label for="email">Email</label>
            <input id="email" />
          </div>
          <div class="info">
            <label for="dateofbirth">Date of Birth</label>
            <input id="dateofbirth" />
          </div>
        </section>
 ```

## 21

- Keeping in mind best-practices for form inputs, give each input an appropriate type and name attribute. Then, give the first input a placeholder attribute.

```html
<section role="region" aria-labelledby="student-info">
          <h2 id="student-info">Student Info</h2>
          <div class="info">
            <label for="student-name">Name:</label>
            <input id="student-name" name="name" placeholder="Name" />
          </div>
          <div class="info">
            <label for="student-email">Email:</label>
            <input id="student-email" type="email" name="email" placeholder="email" />
          </div>
          <div class="info">
            <label for="birth-date">Date of Birth:</label>
            <input id="birth-date" type="date" name="birthdate" placeholder="Date of birth" />
          </div>
        </section>
 ```

## 22

- Even though you added a placeholder to the first input element in the previous lesson, this is actually not a best-practice for accessibility; too often, users confuse the placeholder text with an actual input value - they think there is already a value in the input.

- Remove the placeholder text from the first input element, relying on the label being the best-practice.

```html
<div class="info">
            <label for="student-name">Name:</label>
            <input type="text" name="student-name" id="student-name" />
          </div>
 ```

## 23

- Within the second section element, add two div elements with a class of question-block.

- Then, within each div.question-block element, add one h3 element with text of incrementing numbers, starting at 1, and one fieldset element with a class of question.

```html
<section role="region" aria-labelledby="html-questions">
          <h2 id="html-questions">HTML</h2>
          <div class="question-block"><h3>1</h3><fieldset class="question"></fieldset></div>
          <div class="question-block"><h3>2</h3><fieldset class="question"></fieldset></div>
        </section>
 ```

## 24

- The question numbers are not descriptive enough. This is especially true for visually impaired users. One way to get around such an issue, without having to add visible text to the element, is to add text only a screen reader can read.

- Append a span element with a class of sr-only to each of the h3 elements.

```html
<h3><span class="sr-only">1</span></h3>
            <fieldset class="question"></fieldset>
          </div>
          <div class="question-block">
            <h3><span class="sr-only">2</span></h3>
 ```

## 25

- Within the first span element, add the text Question.

- In the second span element, add the text Question.

```html
<h3><span class="sr-only">Question</span>1</h3>
            <fieldset class="question"></fieldset>
          </div>
          <div class="question-block">
            <h3><span class="sr-only">Question</span>2</h3>
 ```

## 26

- The .sr-only text is still visible. There is a common pattern to visually hide text for only screen readers to read.

This pattern is to set the following CSS properties:

Example Code
position: absolute;
width: 1px;
height: 1px;
padding: 0;
margin: -1px;
overflow: hidden;
clip: rect(0, 0, 0, 0);
white-space: nowrap;
border: 0;
Use the above to define the .sr-only CSS rule.

```html
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
 ```

## 27

- Each fieldset will contain a true/false question.

- Within each fieldset, nest one legend element, and one ul element with two options.

```html
<section role="region" aria-labelledby="html-questions">
          <h2 id="html-questions">HTML</h2>
          <div class="question-block">
            <h3><span class="sr-only"></span>1</h3>
            <fieldset class="question"><legend></legend><ul><li></li><li></li></ul></fieldset>
          </div>
          <div class="question-block">
            <h3><span class="sr-only"></span>2</h3>
            <fieldset class="question"><legend></legend><ul><li></li><li></li></ul></fieldset>
          </div>
        </section>
 ```

## 28

- Give each fieldset an adequate name attribute. Then, give both unordered lists a class of answers-list.

- Finally, use the legend to caption the content of the fieldset by placing a true/false question as the text content.

```html
<section role="region" aria-labelledby="html-questions">
          <h2 id="html-questions">HTML</h2>
          <div class="question-block">
            <h3><span class="sr-only">Question</span>1</h3>
            <fieldset class="question" name="1">
              <legend>True</legend>
              <ul class="answers-list">
                <li></li>
                <li></li>
              </ul>
            </fieldset>
          </div>
          <div class="question-block">
            <h3><span class="sr-only">Question</span>2</h3>
            <fieldset class="question" name="2">
              <legend>False</legend>
              <ul class="answers-list">
                <li></li>
                <li></li>
              </ul>
            </fieldset>
          </div>
        </section>
```

## 29

- To provide the functionality of the true/false questions, we need a set of inputs which do not allow both to be selected at the same time.

- Within each list element, nest one label element, and within each label element, nest one input element with the appropriate type.

```html
<ul class="answers-list">
                <li><label><input type="radio" /></label></li>
                <li><label><input type="radio" /></label></li>
              </ul>
            </fieldset>
          </div>
          <div class="question-block">
            <h3><span class="sr-only">Question</span>2</h3>
            <fieldset class="question" name="html-question-two">
              <legend>
                A label element nesting an input element is required to have a
                for attribute with the same value as the input's id
              </legend>
              <ul class="answers-list">
                <li><label><input type="radio" /></label></li>
                <li><label><input type="radio" /></label></li>
              </ul>
```

## 30

- Add an id to all of your radio inputs so you can link your labels to them. Give the first one an id of q1-a1. Give the rest of them ids of q1-a2, q2-a1, and q2-a2, respectively.

```html
<ul class="answers-list">
                <li>
                  <label>
                    <input type="radio" id="q1-a1" />
                  </label>
                </li>
                <li>
                  <label>
                    <input type="radio" id="q1-a2" />
                  </label>
                </li>
              </ul>
            </fieldset>
          </div>
          <div class="question-block">
            <h3><span class="sr-only">Question</span>2</h3>
            <fieldset class="question" name="html-question-two">
              <legend>
                A label element nesting an input element is required to have a
                for attribute with the same value as the input's id
              </legend>
              <ul class="answers-list">
                <li>
                  <label>
                    <input type="radio" id="q2-a1" />
                  </label>
                </li>
                <li>
                  <label>
                    <input type="radio" id="q2-a2" />
                  </label>
                </li>
              </ul>
```

## 31

- Although not required for label elements with a nested input, it is still best-practice to explicitly link a label with its corresponding input element.

- Now, add a for attribute to each of your four labels that links the label to its corresponding radio input.

```html
<ul class="answers-list">
                <li>
                  <label for="q1-a1">
                    <input type="radio" id="q1-a1"/>
                  </label>
                </li>
                <li>
                  <label for="q1-a2">
                    <input type="radio" id="q1-a2" />
                  </label>
                </li>
              </ul>
            </fieldset>
          </div>
          <div class="question-block">
            <h3><span class="sr-only">Question</span>2</h3>
            <fieldset class="question" name="html-question-two">
              <legend>
                A label element nesting an input element is required to have a
                for attribute with the same value as the input's id
              </legend>
              <ul class="answers-list">
                <li>
                  <label for="q2-a1">
                    <input type="radio" id="q2-a1" />
                  </label>
                </li>
                <li>
                  <label for="q2-a2">
                    <input type="radio" id="q2-a2" />
                  </label>
                </li>
              </ul>
```

## 32

- Give the label elements text such that the input comes before the text. Then, give the input elements a value matching the text.

- The text should either be True or False.

```html
<ul class="answers-list">
                <li>
                  <label for="q1-a1">
                    <input type="radio" id="q1-a1" value="true" />True
                  </label>
                </li>
                <li>
                  <label for="q1-a2">
                    <input type="radio" id="q1-a2" value="false" />False
                  </label>
                </li>
              </ul>
            </fieldset>
          </div>
          <div class="question-block">
            <h3><span class="sr-only">Question</span>2</h3>
            <fieldset class="question" name="html-question-two">
              <legend>
                A label element nesting an input element is required to have a
                for attribute with the same value as the input's id
              </legend>
              <ul class="answers-list">
                <li>
                  <label for="q2-a1">
                    <input type="radio" id="q2-a1" value="true" />True
                  </label>
                </li>
                <li>
                  <label for="q2-a2">
                    <input type="radio" id="q2-a2" value="false" />False
                  </label>
                </li>
              </ul>
```

## 33

- If you click on the radio inputs, you might notice both inputs within the same true/false fieldset can be selected at the same time.

- Group the relevant inputs together such that only one input from a pair can be selected at a time.

```html
<ul class="answers-list">
                <li>
                  <label for="q1-a1">
                    <input type="radio" id="q1-a1" value="true" name="quest" />
                    True
                  </label>
                </li>
                <li>
                  <label for="q1-a2">
                    <input type="radio" id="q1-a2" value="false" name="quest" />
                    False
                  </label>
                </li>
              </ul>
            </fieldset>
          </div>
          <div class="question-block">
            <h3><span class="sr-only">Question</span>2</h3>
            <fieldset class="question" name="html-question-two">
              <legend>
                A label element nesting an input element is required to have a
                for attribute with the same value as the input's id
              </legend>
              <ul class="answers-list">
                <li>
                  <label for="q2-a1">
                    <input type="radio" id="q2-a1" value="true" name="quests" />
                    True
                  </label>
                </li>
                <li>
                  <label for="q2-a2">
                    <input type="radio" id="q2-a2" value="false" name="quests" />
                    False
                  </label>
                </li>
              </ul>
```

## 34

- To prevent unnecessary repetition, target the before pseudo-element of the h3 element, and give it a content property of "Question #".

```html
h3::before {
  content: "Question #"
}
```

## 35

- Create a new .left-container p selector setting the top and bottom margin to -5px, and the left and right margin to -2px. Also set the font-size to 2em and font-weight to 700.

```html
.left-container p {
  margin: -5px -2px;
  font-size: 2em;
  font-weight: 700;
}
```

## 36

- Create a .calories-info span selector, set its font-size to 2.4em and font-weight to 700.

```html
.calories-info span {
  font-size: 2.4em;
  font-weight: 700;
}
```

## 37

- Typography is often more art than science. You may have to tweak things like alignment until it looks correct.

- Give your .calories-info span selector a margin set to -7px -2px. This will shift your 230 text into place.

```html
.calories-info span {
  font-size: 2.4em;
  font-weight: 700;
  margin: -7px -2px;
}
```

## 38

- Below your .calories-info element, add a div with the class attribute set to divider medium.

```html
<div class="divider medium">
```

## 39

- Create an .medium selector and give it a height property of 5px.

```html
.medium {
  height: 5px;
}
```

## 40

- Create a new div element below your .medium element. Give it a class attribute set to daily-value small-text. Within this new div, add a p element with the text % Daily Value *, and set the class attribute to bold right.

```html
<div class="divider medium"></div>
    <div class="daily-value small-text">
      <p class="bold right">% Daily Value *</p>
    </div>
```

## 41

- The text % Daily Value * should be aligned to the right. Create a .right selector and use the justify-content property to do it.

```html
.right {
  justify-content: flex-end;
}
```

## 42

- Use your existing .divider element as an example to add a new divider after the p element.

```html
<div class="daily-value small-text">
      <p class="bold right">% Daily Value *</p>
      <div class="divider"></div>
    </div>
```

## 43

- After your last .divider element, create a p element and give it the text Total Fat 8g 10%. Then, wrap the text Total Fat in one span element, the text 10% in another, and give them each a class of bold.

```html
<div class="daily-value small-text">
      <p class="bold right">% Daily Value *</p>
      <div class="divider"></div>
      <p class="bold right"><span class="bold">Total Fat</span> 8g <span class="bold">10%</span></p>
    </div>
```

## 44

- Notice how the text 8g appears centered in the preview. Nest the span element containing the text Total Fat along with the text 8g, in an additional span element for alignment.

```html
<p><span class="bold"><span class="bold">Total Fat</span> 8g</span> <span class="bold">10%</span></p>
```

## 45

- Below your element with the Total Fat text, create a new p element with the text Saturated Fat 1g 5%. Wrap the 5% in a span with the class attribute set to bold. In this case this is enough to align the percentage to 5%.

```html
<div class="daily-value small-text">
      <p class="bold right">% Daily Value *</p>
      <div class="divider"></div>
      <p><span><span class="bold">Total Fat</span> 8g</span> <span class="bold">10%</span></p>
      <p>Saturated Fat 1g <span class="bold">5%</span></p>
    </div>
```

## 46

- This new p element will need to be indented. Give it a class set to indent.

```html
<div class="daily-value small-text">
      <p class="bold right">% Daily Value *</p>
      <div class="divider"></div>
      <p><span><span class="bold">Total Fat</span> 8g</span> <span class="bold">10%</span></p>
      <p class="indent">Saturated Fat 1g <span class="bold">5%</span></p>
    </div>
```

## 47

- Create a new .indent selector and give it a margin-left property set to 1em.

```html
.indent {
  margin-left: 1em;
}
```

## 48

- Create a .daily-value p selector to target all of your p elements in the daily-value section. Give this new selector a border-bottom set to 1px solid #888989.

```html

daily-value p {
  border-bottom: 1px solid #888989;
}

```

## 49

- The bottom borders under your % Daily Value * and Saturated Fat 1g 5% elements do not extend the full width of the label. Add no-divider to the class for these two elements.

```html

<div class="daily-value small-text">
      <p class="bold right no-divider">% Daily Value *</p>
      <div class="divider"></div>
      <p><span><span class="bold">Total Fat</span> 8g</span> <span class="bold">10%</span></p>
      <p class="indent no-divider">Saturated Fat 1g <span class="bold">5%</span></p>
    </div>

```

## 50

- The :not pseudo-selector can be used to select all elements that do not match the given CSS rule.

Example Code
div:not(#example) {
  color: red;
}
The above selects all div elements without an id of example.

Modify your .daily-value p selector to exclude the .no-divider elements.

```html

.daily-value p:not(.no-divider) {
  border-bottom: 1px solid #888989;
}
          
```

## 51

- Now you will have to add separate dividers below your .no-divider elements.

- Your first .no-divider element has a .divider after it. Create another .divider after your second .no-divider element.

```html

<div class="daily-value small-text">
      <p class="bold right no-divider">% Daily Value *</p>
      <div class="divider"></div>
      <p><span><span class="bold">Total Fat</span> 8g</span> <span class="bold">10%</span></p>
      <p class="indent no-divider">Saturated Fat 1g <span class="bold">5%</span></p>
      <div class="divider"></div>
    </div>   
          
```

## 52

- After your last .divider, create another p element with the text Trans Fat 0g. Italicize the word Trans by wrapping it in an i element. Give the new p element the class attribute set to indent no-divider. Wrap Trans Fat 0g in a span element for alignment.

```html

<div class="daily-value small-text">
      <p class="bold right no-divider">% Daily Value *</p>
      <div class="divider"></div>
      <p><span><span class="bold">Total Fat</span> 8g</span> <span class="bold">10%</span></p>
      <p class="indent no-divider">Saturated Fat 1g <span class="bold">5%</span></p>
      <div class="divider"></div>
      <p class="indent no-divider"><span><i>Trans</i> Fat 0g</span></p>
    </div>   
          
```

## 53

- Create another .divider after your last p element.

```html

<div class="daily-value small-text">
      <p class="bold right no-divider">% Daily Value *</p>
      <div class="divider"></div>
      <p><span><span class="bold">Total Fat</span> 8g</span> <span class="bold">10%</span></p>
      <p class="indent no-divider">Saturated Fat 1g <span class="bold">5%</span></p>
      <div class="divider"></div>
      <p class="indent no-divider"><span><i>Trans</i> Fat 0g</span></p>
      <div class="divider"></div>
    </div>    

```

## 54

- After your last .divider, create a new p element with the text Cholesterol 0mg 0%. Then, wrap the text Cholesterol in a span element, 0% in another, and give each of them a class of bold.

- Finally, nest the span element containing the text Cholesterol along with the text 0mg, in an additional span element for alignment.

```html

<div class="daily-value small-text">
      <p class="bold right no-divider">% Daily Value *</p>
      <div class="divider"></div>
      <p><span><span class="bold">Total Fat</span> 8g</span> <span class="bold">10%</span></p>
      <p class="indent no-divider">Saturated Fat 1g <span class="bold">5%</span></p>
      <div class="divider"></div>
      <p class="indent no-divider"><span><i>Trans</i> Fat 0g</span></p>
      <div class="divider"></div>
      <p><span><span class="bold">Cholesterol</span> 0mg</span> <span class="bold">0%</span></p>
    </div>   
```

## 55

- Below your last p element, create another p element with the text Sodium 160mg 7%. Put Sodium and 7% each in their own span with a class of a bold like you did with the others.

- Then, add an additional span element around Sodium 160mg for alignment again.

```html

<div class="daily-value small-text">
      <p class="bold right no-divider">% Daily Value *</p>
      <div class="divider"></div>
      <p><span><span class="bold">Total Fat</span> 8g</span> <span class="bold">10%</span></p>
      <p class="indent no-divider">Saturated Fat 1g <span class="bold">5%</span></p>
      <div class="divider"></div>
      <p class="indent no-divider"><span><i>Trans</i> Fat 0g</span></p>
      <div class="divider"></div>
      <p><span><span class="bold">Cholesterol</span> 0mg</span> <span class="bold">0%</span></p>
      <p><span><span class="bold">Sodium</span> 160mg</span> <span class="bold">7%</span></p>
    </div>    

```

## 56

- Below your last p element, add another p element with the text Total Carbohydrate 37g 13%. Like before, use span elements to make the text Total Carbohydrate and 13% bold. Then, wrap the nutrient and amount in a span for alignment again.

```html

<div class="daily-value small-text">
      <p class="bold right no-divider">% Daily Value *</p>
      <div class="divider"></div>
      <p><span><span class="bold">Total Fat</span> 8g</span> <span class="bold">10%</span></p>
      <p class="indent no-divider">Saturated Fat 1g <span class="bold">5%</span></p>
      <div class="divider"></div>
      <p class="indent no-divider"><span><i>Trans</i> Fat 0g</span></p>
      <div class="divider"></div>
      <p><span><span class="bold">Cholesterol</span> 0mg</span> <span class="bold">0%</span></p>
      <p><span><span class="bold">Sodium</span> 160mg</span> <span class="bold">7%</span></p>
      <p><span><span class="bold">Total Carbohydrate</span> 37g</span> <span class="bold">13%</span></p>
    </div>    

```

## 57

- Below your last p element, add another p element with the text Dietary Fiber 4g. Give the p element the class necessary to indent it and remove the dividing border. Then create a divider below that p element.

```html

<div class="daily-value small-text">
      <p class="bold right no-divider">% Daily Value *</p>
      <div class="divider"></div>
      <p><span><span class="bold">Total Fat</span> 8g</span> <span class="bold">10%</span></p>
      <p class="indent no-divider">Saturated Fat 1g <span class="bold">5%</span></p>
      <div class="divider"></div>
      <p class="indent no-divider"><span><i>Trans</i> Fat 0g</span></p>
      <div class="divider"></div>
      <p><span><span class="bold">Cholesterol</span> 0mg</span> <span class="bold">0%</span></p>
      <p><span><span class="bold">Sodium</span> 160mg</span> <span class="bold">7%</span></p>
      <p><span><span class="bold">Total Carbohydrate</span> 37g</span> <span class="bold">13%</span></p>
      <p class="indent no-divider">Dietary Fiber 4g</p>
      <div class="divider"></div>
    </div>    

```

## 58

- Create another p element after your last .divider, and give it the text Total Sugars 12g. Assign that p element the class values necessary to indent it and remove the bottom border. Then create another .divider below your new p element.

```html

<div class="daily-value small-text">
      <p class="bold right no-divider">% Daily Value *</p>
      <div class="divider"></div>
      <p><span><span class="bold">Total Fat</span> 8g</span> <span class="bold">10%</span></p>
      <p class="indent no-divider">Saturated Fat 1g <span class="bold">5%</span></p>
      <div class="divider"></div>
      <p class="indent no-divider"><span><i>Trans</i> Fat 0g</span></p>
      <div class="divider"></div>
      <p><span><span class="bold">Cholesterol</span> 0mg</span> <span class="bold">0%</span></p>
      <p><span><span class="bold">Sodium</span> 160mg</span> <span class="bold">7%</span></p>
      <p><span><span class="bold">Total Carbohydrate</span> 37g</span> <span class="bold">13%</span></p>
      <p class="indent no-divider">Dietary Fiber 4g</p>
      <div class="divider"></div>
      <p class="indent no-divider">Total Sugars 12g</p>
       <div class="divider"></div>
    </div>    

```

## 59

- The advantage to creating these dividers is that you can apply specific classes to style them individually. Add double-indent to the class for your last .divider.

```html

<div class="divider double-indent"></div>
 ```

## 60

- Create a .double-indent selector and give it a left margin of 2em.

```html

.double-indent {
  margin-left: 2em;
}
 ```

## 61

- Below your .double-indent element, add a new p element with the text Includes 10g Added Sugars 20%. Your new p element should also be double indented, and have no bottom border. Use a span to make the 20% bold and right aligned.

- Then create another divider after that p element.

```html

<div class="daily-value small-text">
      <p class="bold right no-divider">% Daily Value *</p>
      <div class="divider"></div>
      <p><span><span class="bold">Total Fat</span> 8g</span> <span class="bold">10%</span></p>
      <p class="indent no-divider">Saturated Fat 1g <span class="bold">5%</span></p>
      <div class="divider"></div>
      <p class="indent no-divider"><span><i>Trans</i> Fat 0g</span></p>
      <div class="divider"></div>
      <p><span><span class="bold">Cholesterol</span> 0mg</span> <span class="bold">0%</span></p>
      <p><span><span class="bold">Sodium</span> 160mg</span> <span class="bold">7%</span></p>
      <p><span><span class="bold">Total Carbohydrate</span> 37g</span> <span class="bold">13%</span></p>
      <p class="indent no-divider">Dietary Fiber 4g</p>
      <div class="divider"></div>
      <p class="indent no-divider">Total Sugars 12g</p>
      <div class="divider double-indent"></div>
      <p class="double-indent no-divider">Includes 10g Added Sugars <span class="bold right">20%</span></p>
      <div class="divider double-indent"></div>
    </div>

 ```

## 62

- After your last divider, create another p element with the text Protein 3g. Use the necessary classes to remove the bottom border, and a span to make the Protein bold. Then wrap the text Protein 3g including the new span element, in a new span element.

- Following this element, create a large divider.

```html

<div class="daily-value small-text">
      <p class="bold right no-divider">% Daily Value *</p>
      <div class="divider"></div>
      <p><span><span class="bold">Total Fat</span> 8g</span> <span class="bold">10%</span></p>
      <p class="indent no-divider">Saturated Fat 1g <span class="bold">5%</span></p>
      <div class="divider"></div>
      <p class="indent no-divider"><span><i>Trans</i> Fat 0g</span></p>
      <div class="divider"></div>
      <p><span><span class="bold">Cholesterol</span> 0mg</span> <span class="bold">0%</span></p>
      <p><span><span class="bold">Sodium</span> 160mg</span> <span class="bold">7%</span></p>
      <p><span><span class="bold">Total Carbohydrate</span> 37g</span> <span class="bold">13%</span></p>
      <p class="indent no-divider">Dietary Fiber 4g</p>
      <div class="divider"></div>
      <p class="indent no-divider">Total Sugars 12g</p>
      <div class="divider double-indent"></div>
      <p class="double-indent no-divider">Includes 10g Added Sugars <span class="bold">20%</span></p>
      <div class="divider"></div>
      <p class="no-divider"><span><span class="bold">Protein</span> 3g</span></p>
      <div class="divider large"></div>
    </div>

 ```

## 63

- Create another p element below your large divider. Give the p element the text Vitamin D 2mcg 10%.

- The p element contains only text, you can wrap the percentage in a span element so that it is considered a separate entity from the rest of the text, and it's moved to the right.

```html

<div class="daily-value small-text">
      <p class="bold right no-divider">% Daily Value *</p>
      <div class="divider"></div>
      <p><span><span class="bold">Total Fat</span> 8g</span> <span class="bold">10%</span></p>
      <p class="indent no-divider">Saturated Fat 1g <span class="bold">5%</span></p>
      <div class="divider"></div>
      <p class="indent no-divider"><span><i>Trans</i> Fat 0g</span></p>
      <div class="divider"></div>
      <p><span><span class="bold">Cholesterol</span> 0mg</span> <span class="bold">0%</span></p>
      <p><span><span class="bold">Sodium</span> 160mg</span> <span class="bold">7%</span></p>
      <p><span><span class="bold">Total Carbohydrate</span> 37g</span> <span class="bold">13%</span></p>
      <p class="indent no-divider">Dietary Fiber 4g</p>
      <div class="divider"></div>
      <p class="indent no-divider">Total Sugars 12g</p>
      <div class="divider double-indent"></div>
      <p class="double-indent no-divider">Includes 10g Added Sugars <span class="bold">20%</span></p>
      <div class="divider"></div>
      <p class="no-divider"><span><span class="bold">Protein</span> 3g</span></p>
      <div class="divider large"></div>
      <p>Vitamin D 2mcg <span>10%</span></p>
    </div>

 ```

## 64

- Create another p element, give it the text Calcium 260mg 20%. Align 20% to the right. Below that, create a p element with the text Iron 8mg 45%, aligning the 45% to the right.

```html
<div class="daily-value small-text">
      <p class="bold right no-divider">% Daily Value *</p>
      <div class="divider"></div>
      <p><span><span class="bold">Total Fat</span> 8g</span> <span class="bold">10%</span></p>
      <p class="indent no-divider">Saturated Fat 1g <span class="bold">5%</span></p>
      <div class="divider"></div>
      <p class="indent no-divider"><span><i>Trans</i> Fat 0g</span></p>
      <div class="divider"></div>
      <p><span><span class="bold">Cholesterol</span> 0mg</span> <span class="bold">0%</span></p>
      <p><span><span class="bold">Sodium</span> 160mg</span> <span class="bold">7%</span></p>
      <p><span><span class="bold">Total Carbohydrate</span> 37g</span> <span class="bold">13%</span></p>
      <p class="indent no-divider">Dietary Fiber 4g</p>
      <div class="divider"></div>
      <p class="indent no-divider">Total Sugars 12g</p>
      <div class="divider double-indent"></div>
      <p class="double-indent no-divider">Includes 10g Added Sugars <span class="bold">20%</span></p>
      <div class="divider"></div>
      <p class="no-divider"><span><span class="bold">Protein</span> 3g</span></p>
      <div class="divider large"></div>
      <p>Vitamin D 2mcg <span>10%</span></p>
      <p>Calcium 260mg <span class="right">20%</span></p>
      <p>Iron 8mg <span class="right">45%</span></p>
    </div>
```

## 65

- Create the final p element for your .daily-value section. Give it the text Potassium 235mg 6%. Align the 6% text to the right, and remove the bottom border of the p element.

```html
<div class="daily-value small-text">
      <p class="bold right no-divider">% Daily Value *</p>
      <div class="divider"></div>
      <p><span><span class="bold">Total Fat</span> 8g</span> <span class="bold">10%</span></p>
      <p class="indent no-divider">Saturated Fat 1g <span class="bold">5%</span></p>
      <div class="divider"></div>
      <p class="indent no-divider"><span><i>Trans</i> Fat 0g</span></p>
      <div class="divider"></div>
      <p><span><span class="bold">Cholesterol</span> 0mg</span> <span class="bold">0%</span></p>
      <p><span><span class="bold">Sodium</span> 160mg</span> <span class="bold">7%</span></p>
      <p><span><span class="bold">Total Carbohydrate</span> 37g</span> <span class="bold">13%</span></p>
      <p class="indent no-divider">Dietary Fiber 4g</p>
      <div class="divider"></div>
      <p class="indent no-divider">Total Sugars 12g</p>
      <div class="divider double-indent"></div>
      <p class="double-indent no-divider">Includes 10g Added Sugars <span class="bold">20%</span></p>
      <div class="divider"></div>
      <p class="no-divider"><span><span class="bold">Protein</span> 3g</span></p>
      <div class="divider large"></div>
      <p>Vitamin D 2mcg <span>10%</span></p>
      <p>Calcium 260mg <span>20%</span></p>
      <p>Iron 8mg <span>45%</span></p>
      <p class="no-divider">Potassium 235mg <span>6%</span></p>
    </div>
```

## 66

- Add a medium divider after your .daily-value element. Below that new divider, create a p element with the class attribute set to note.

Give the p element the following text:

Example Code
<!-- * The % Daily Value (DV) tells you how much a nutrient in a serving of food contributes to a daily diet. 2,000 calories a day is used for general nutrition advice. -->

```html
<div class="divider medium"></div>
<p class="note">* The % Daily Value (DV) tells you how much a nutrient in a serving of food contributes to a daily diet. 2,000 calories a day is used for general nutrition advice.</p>
```

## 67

- Create a .note selector, and set the size of the font to 0.6rem. Also set the top and bottom margins to 5px, removing the left and right margins.

```html
.note {
  font-size: 0.6rem;
  margin: 5px 0;
}
```

## 68

- Give the .note selector a left and right padding of 8px, removing the top and bottom padding. Also set the text-indent property to -8px.

- With these last changes, your nutrition label is complete!

```html

.note {
  font-size: 0.6rem;
  margin: 5px 0;
  padding: 0 8px;
  text-indent: -8px;
}
```
