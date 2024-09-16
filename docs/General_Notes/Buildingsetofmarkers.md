# Building set of markers

## 1. Tags

- As you've seen in the previous projects, webpages should start with a DOCTYPE html declaration, followed by an html element.

- Add a DOCTYPE html declaration at the top of the document, and an html element after that. Give the html element a lang attribute with en as its value.

```html
<!DOCTYPE html>
<html lang="en">
</html>
```

## 2

```html
- Nest a head element within the html element. Just after the head element, add a body element.

<head>
</head>
<body>
</body>
```

## 3

- Remember that the title element gives search engines extra information about the page. It also displays the content of that title element in two more ways:

- in the title bar when the page is open
- in the browser tab for the page when you hover on it. Even if that tab is not active, once you hover on the tab, the title text is displayed.
- Within the head element, nest a title element with the text Colored Markers.

```html
<head>
    <title> Colored Markers </title>
  </head>
```

## 4

```html
The charset attribute specifies the character encoding used by the document. utf-8 (Unicode Transformation Format – 8-bit) is a character encoding standard used for electronic communication.

Inside the head element, nest a meta element with the attribute charset set to "utf-8".

<head>
    <title>Colored Markers</title>
    <meta charset="utf-8">
  </head>
```

## 5

```html
- You can have multiple meta elements on a web page. Each meta element adds information about the page that cannot be expressed by other HTML elements.

Add another meta element within the head. Give it a name attribute set to "viewport" and a content attribute set to "width=device-width, initial-scale=1.0" so your page looks the same on all devices.

<head>
    <meta name="viewport" content="width=device-width,initial-scale=1.0">
    <meta charset="utf-8">
    <title>Colored Markers</title>
  </head>
```

## 6

```html
- Now you're ready to start adding content to the page.

- Within the body, nest an h1 element with the text CSS Color Markers.

<body>
    <h1> CSS Color Markers </h1>
  </body>
```

## 7

```html
- In this project you'll work with an external CSS file to style the page. We've already created a styles.css file for you. But before you can use it, you'll need to link it to the page.

- Nest a link element within the head element. Give it a rel attribute set to "stylesheet" and an href attribute set to "styles.css".

<head>
    <link rel="stylesheet" href="styles.css">
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Colored Markers</title>
  </head>

```

## 8

```html
- Create a new CSS rule that targets the h1 element, and set its text-align property to center.
h1 {
  text-align: center;
}
```

## 9

```html
- Now you'll add some elements that you'll eventually style into color markers.

- First, within the body element, add a div element and set its class attribute to container. Make sure the div element is below the h1 element.

<body>
    <h1>CSS Color Markers</h1>
    <div class="container"></div>
  </body>
```

## 10

- Next, within the div element, add another div element and give it a class of marker.

```html
<body>
    <h1>CSS Color Markers</h1>
    <div class="container">
      <div class="marker"></div>
    </div>
  </body>
```

## 11

- It's time to add some color to the marker. Remember that one way to add color to an element is to use a color keyword like black, cyan, or yellow.

- As a reminder, here's how to target the class freecodecamp:

 Example Code
 .freecodecamp {
  
 }

- Create a new CSS rule that targets the class marker, and set its background-color property to red.

```html

.marker {
  background-color:red;
}

```

## 12

- The background color was applied, but since the marker div element has no content in it, it doesn't have any height by default.

- In your .marker CSS rule, set the height property to 25px and the width property to 200px

```html
.marker {
  background-color: red;
  height: 25px;
  width: 200px;
}
```

## 13

- Your marker would look better if it was centered on the page. An easy way to do that is with the margin shorthand property.

- In the last project, you set the margin area of elements separately with properties like margin-top and margin-left. The margin shorthand property makes it easy to set multiple margin areas at the same time.

- To center your marker on the page, set its margin property to auto. This sets margin-top, margin-right, margin-bottom, and margin-left all to auto.

```html
.marker {
  width: 200px;
  height: 25px;
  background-color: red;
  margin: auto;
}
```

## 14

- This works, but since there will be many more styles, it's best to put all the styles in a separate file and link to it.

```html
<div class="container">
      <div class="marker">
      </div>
      <div class="marker">
      </div>
      <div class="marker">
      </div>
    </div>
```

## 15

- While you have three separate marker div elements, they look like one big rectangle. You should add some space between them to make it easier to see each element.

- When the shorthand margin property has two values, it sets margin-top and margin-bottom to the first value, and margin-left and margin-right to the second value.

- In your .marker CSS rule, set the margin property to 10px auto.

```html
.marker {
  width: 200px;
  height: 25px;
  background-color: red;
  margin: 10px auto;
}
```

## 16

- To give the markers different colors, you will need to add a unique class to each one. Multiple classes can be added to an element by listing them in the class attribute and separating them with a space. For example, the following adds both the animal and dog classes to a div element.

Example Code

```html
<div class="animal dog">
```

If you add multiple classes to an HTML element, the styles of the first classes you list may be overridden by later classes.

To begin, add the class one to the first marker div element.

```html
 <div class="marker one">
      </div>
      <div class="marker">
      </div>
      <div class="marker">
      </div>
```

## 17

- Next, remove the background-color property and its value from the .marker CSS rule.

```html
.marker {
  width: 200px;
  height: 25px;
  margin: 10px auto;
}
```

## 18

- Then, create a new CSS rule that targets the class one and set its background-color property to red.

```html
.one {
  background-color:red;
}
```

## 19

- Add the class two to the second marker div, and add the class three to the third marker div.

```html
<div class="marker one">
      </div>
      <div class="marker two">
      </div>
      <div class="marker three">
      </div>
```

## 20

- Create a CSS rule that targets the class two and set its background-color property to green.

- Also, create a separate CSS rule that targets the class three and set its background-color to blue.

```html
.two {
  background-color: green;
}

.three {
  background-color: blue;
}
 ```

## 21

- There are two main color models: the additive RGB (red, green, blue) model used in electronic devices, and the subtractive CMYK (cyan, magenta, yellow, black) model used in print.

- In this project, you'll work with the RGB model. This means that colors begin as black, and change as different levels of red, green, and blue are introduced. An easy way to see this is with the CSS rgb function.

- Create a new CSS rule that targets the class container and set its background-color to black with rgb(0, 0, 0).

```html
.container{
  background-color: rgb(0, 0, 0);
}
 ```

## 22

```html
- A function is a piece of code that can take an input and perform a specific action. The CSS rgb function accepts values, or arguments, for red, green, and blue, and produces a color:

Example Code
- rgb(red, green, blue);
- Each red, green, and blue value is a number from 0 to 255. 0 means that there's 0% of that color, and is black. 255 means that there's 100% of that color.

- In the .one CSS rule, replace the color keyword red with the rgb function. For the rgb function, set the value for red to 255, the value for green to 0, and the value for blue to 0.

.one {
  background-color: rgb(255, 0, 0);
}
 ```

## 23

```html
- Notice that the background-color for your marker is still red. This is because you set the red value of the rgb function to the max of 255, or 100% red, and set both the green and blue values to 0.

Now use the rgb function to set the other colors.

In the .two CSS rule, use the rgb function to set the background-color to the max value for green, and 0 for the other values. And in the .three CSS rule, use the rgb function to set the background-color to the max value for blue, and 0 for the other values.

.two {
  background-color: rgb(0, 255, 0);
}

.three {
  background-color: rgb(0, 0, 255);
}
 ```

## 24

- While the red and blue markers look the same, the green one is much lighter than it was before. This is because the green color keyword is actually a darker shade, and is about halfway between black and the maximum value for green.

- In the .two CSS rule, set the green value in the rgb function to 127 to lower its intensity.

```html
.two {
  background-color: rgb(0, 127, 0);
}
 ```

## 25

- Now add a little more vertical space between your markers and the edge of the container element they're in.

- In the .container CSS rule, use the shorthand padding property to add 10px of top and bottom padding, and set the left and right padding to 0. This works similarly to the shorthand margin property you used earlier.

```html
.container {
  background-color: rgb(0, 0, 0);
  padding: 10px 0px;
}
 ```

## 26

- In the additive RGB color model, primary colors are colors that, when combined, create pure white. But for this to happen, each color needs to be at its highest intensity.

- Before you combine colors, set your green marker back to pure green. For the rgb function in the .two CSS rule, set green back to the max value of 255.

```html
.two {
  background-color: rgb(0, 255, 0);
}
 ```

## 27

- Now that you have the primary RGB colors, it's time to combine them.

- For the rgb function in the .container rule, set the red, green, and blue values to the max of 255.

```html
 .container {
  background-color: rgb(255, 255, 255);
  padding: 10px 0;
}
 ```

## 28

- Secondary colors are the colors you get when you combine primary colors. You might have noticed some secondary colors in the last step as you changed the red, green, and blue values.

- To create the first secondary color, yellow, update the rgb function in the .one CSS rule to combine pure red and pure green.

```html
.one {
  background-color: rgb(255, 255, 0);
}
```

## 29

- To create the next secondary color, cyan, update the rgb function in the .two CSS rule to combine pure green and pure blue.

```html
.two {
  background-color: rgb(0, 255, 255);
}
```

## 30

- To create the final secondary color, magenta, update the rgb function in the .three CSS rule to combine pure blue and pure red.

```html
.three {
  background-color: rgb(255, 0, 255);
}
```

## 31

- Now that you're familiar with secondary colors, you'll learn how to create tertiary colors. Tertiary colors are created by combining a primary with a nearby secondary color.

- To create the tertiary color orange, update the rgb function in the .one CSS rule so that red is at the max value, and set green to 127.

```html
.one {
  background-color: rgb(255, 127, 0);
}
```

## 32

- Notice that, to create orange, you had to increase the intensity of red and decrease the intensity of the green rgb values. This is because orange is the combination of red and yellow.

- To create the tertiary color spring green, combine cyan with green. Update the rgb function in the .two CSS rule so that green is at the max value, and set blue to 127.

```html
.two {
  background-color: rgb(0, 255, 127);
}
```

## 33

- And to create the tertiary color violet, combine magenta with blue. Update the rgb function in the .three CSS rule so that blue is at the max value, and set red to 127.

```html
.three {
  background-color: rgb(127, 0, 255);
}
```

## 34

- There are three more tertiary colors: chartreuse green (green + yellow), azure (blue + cyan), and rose (red + magenta).

- To create chartreuse green, update the rgb function in the .one CSS rule so that red is at 127, and set green to the max value.

- For azure, update the rgb function in the .two CSS rule so that green is at 127 and blue is at the max value.

- And for rose, which is sometimes called bright pink, update the rgb function in the .three CSS rule so that blue is at 127 and red is at the max value.

```html
.one {
  background-color: rgb(127, 255, 0);
}

.two {
  background-color: rgb(0, 127, 255);
}

.three {
  background-color: rgb(255, 0, 127);
}
```

## 35

- Now that you've gone through all the primary, secondary, and tertiary colors on a color wheel, it'll be easier to understand other color theory concepts and how they impact design.

- First, in the CSS rules .one, .two, and .three, adjust the values in the rgb function so that the background-color of each element is set to pure black. Remember that the rgb function uses the additive color model, where colors start as black and change as the values of red, green, and blue increase.

```html
.one {
  background-color: rgb(0, 0, 0);
}

.two {
  background-color: rgb(0, 0, 0);
}

.three {
  background-color: rgb(0, 0, 0);
}
```

## 36

- A color wheel is a circle where similar colors, or hues, are near each other, and different ones are further apart. For example, pure red is between the hues rose and orange.

- Two colors that are opposite from each other on the color wheel are called complementary colors. If two complementary colors are combined, they produce gray. But when they are placed side-by-side, these colors produce strong visual contrast and appear brighter.

- In the rgb function for the .one CSS rule, set the red value to the max of 255 to produce pure red. In the rgb function for .two CSS rule, set the values for green and blue to the max of 255 to produce cyan.

```html
.one {
  background-color: rgb(255, 0, 0);
}

.two {
  background-color: rgb(0, 255, 255);
}
```

## 37

- Notice that the red and cyan colors are very bright right next to each other. This contrast can be distracting if it's overused on a website, and can make text hard to read if it's placed on a complementary-colored background.

- It's better practice to choose one color as the dominant color, and use its complementary color as an accent to bring attention to certain content on the page.

- First, in the h1 rule, use the rgb function to set its background-color to cyan.

```html
h1 {
  background-color: rgb(0, 255, 255);
  text-align: center;
}
```

## 38

- Next, in the .one CSS rule, use the rgb function to set the background-color to black. And in the .two CSS rule, use the rgb function to set the background-color to red.

```html
.one {
  background-color: rgb(0, 0, 0);
}

.two {
  background-color: rgb(255, 0, 0);
}
```

## 39

- Notice how your eyes are naturally drawn to the red color in the center? When designing a site, you can use this effect to draw attention to important headings, buttons, or links.

- There are several other important color combinations outside of complementary colors, but you'll learn those a bit later.

- For now, use the rgb function in the .two CSS rule to set the background-color to black.

```html
.two {
  background-color: rgb(0, 0, 0);
}
```

## 40

- And in the h1 CSS rule, remove the background-color property and value to go back to the default white color.

```html
h1 {
  text-align: center;
}
```

## 41

```html
<!-- changed width back to 50% in the class selectors again, now there is no space from the flavor or price on the menu -->
 .flavor {
  text-align: left;
  width: 50%;
}

.price {
  text-align: right;
  width: 50%;
}
```

## 42

```html
<!-- added the class item to the rest of the articles with a flavor and price -->
 <article class="item">
            <p>Caramel Macchiato</p>
            <p>3.75</p>
          </article>
          <article class="item">
            <p>Pumpkin Spice</p>
            <p>3.50</p>
          </article>
          <article class="item">
            <p>Hazelnut</p>
            <p>4.00</p>
          </article>
          <article class="item">
            <p>Mocha</p>
            <p>4.50</p>
          </article>
```

## 43

```html
<!-- put the other p elements on the same line so there is no space when they are on the sides -->
 <article class="item">
            <p>Caramel Macchiato</p><p>3.75</p>
          </article>
          <article class="item">
            <p>Pumpkin Spice</p><p>3.50</p>
          </article>
          <article class="item">
            <p>Hazelnut</p><p>4.00</p>
          </article>
          <article class="item">
            <p>Mocha</p><p>4.50</p>
          </article>
```

## 44

```html
<!-- added the class elements to each respective flavor and price to add style -->
 <article class="item">
            <p class="flavor">Caramel Macchiato</p><p class="price">3.75</p>
          </article>
          <article class="item">
            <p class="flavor">Pumpkin Spice</p><p class="price">3.50</p>
          </article>
          <article class="item">
            <p class="flavor">Hazelnut</p><p class="price">4.00</p>
          </article>
          <article class="item">
            <p class="flavor">Mocha</p><p class="price">4.50</p>
          </article>
```

## 45

```html
<!-- changed flavor width to 75% and price to 25% to wrap nicely -->
  .flavor {
  text-align: left;
  width: 75%;
}

.price {
  text-align: right;
  width: 25%;
}
```

## 46

```html
<!-- added another section for desserts on the menu -->
  <section></section>
```

## 47

```html
<!-- added h2 element for desserts -->
  <section>
          <h2> Desserts</h2>
        </section>
```

## 48

```html

<!-- added empty article to display desserts and prices with class item -->
  <h2>Desserts</h2>
  <article class="item"></article

```

## 49

```html

<!-- added 2 p elements for dessert and price on the same line -->
  <article class="item">
            <p>Donut</p><p>1.50</p>
          </article>

```

## 50

```html

<!-- added a class for dessert and price in the respective p element -->
  <p class="dessert">Donut</p><p class="price">1.50</p>
          
```

## 51

```html

<!-- added dessert as the additional selector with flavor to apply the same style -->
  .flavor, .dessert {
  text-align: left;
  width: 75%;
}
          
```

## 52

```html

<!-- added the rest of the deserts in their respective artcle element and price -->
          
```

## 53

```html

<!-- You can give your menu some space between the content and the sides with various padding properties.

Give the menu class a padding-left and a padding-right with the same value 20px. --> 
          
.menu {
  width: 80%;
  background-color: burlywood;
  margin-left: auto;
  margin-right: auto;
  padding-left: 20px;
  padding-right: 20px;
}

```

## 54

```html

<!-- added padding to top and bottom --> 
          .menu {
  width: 80%;
  background-color: burlywood;
  margin-left: auto;
  margin-right: auto;
  padding-left: 20px;
  padding-right: 20px;
  padding-top: 20px;
  padding-bottom: 20px;
}
```

## 55

```html

<!-- Since all 4 sides of the menu have the same internal spacing, go ahead and delete the four properties and use a single padding property with the value 20px. -->
.menu {
  width: 80%;
  background-color: burlywood;
  margin-left: auto;
  margin-right: auto;
  padding: 20px;
}

```

## 56

```html

<!-- The current width of the menu will always take up 80% of the body element's width. On a very wide screen, the coffee and dessert appear far apart from their prices.

Add a max-width property to the menu class with a value of 500px to prevent it from growing too wide. -->
 
.menu {
  width: 80%;
  background-color: burlywood;
  margin-left: auto;
  margin-right: auto;
  padding: 20px;
  max-width: 500px;
}

```

## 57

```html

<!-- You can change the font-family of text, to make it look different from the default font of your browser. Each browser has some common fonts available to it.

Change all the text in your body, by adding a font-family property with the value sans-serif. This is a fairly common font that is very readable. -->

body {
  background-image: url(https://cdn.freecodecamp.org/curriculum/css-cafe/beans.jpg);
  font-family: sans-serif;
}

```

## 58

```html

<!-- Style both the h1 and the h2 elements using a single selector so that these elements' text use Impact font. -->
h1,h2 {
font-family: Impact
}

```

## 59

```html

<!-- You can add a fallback value for the font-family by adding another font name separated by a comma. Fallbacks are used in instances where the initial is not found/available.

Add the fallback font serif after the Impact font. -->
h1, h2 {
  font-family: Impact, serif;
}
 ```

## 60

```html

<!-- Make the Est. 2020 text italicized by creating an established class selector and giving it the font-style property with the value italic. -->
.established{
  font-style:italic;
}
 ```

## 61

```html

<!-- Now apply the established class to the Est. 2020 text. -->

<h1>CAMPER CAFE</h1>
        <p class="established">Est. 2020</p>

 ```

## 62

```html

- The typography of heading elements (e.g. h1, h2) is set by default values of users' browsers.

- Add two new type selectors (h1 and h2). Use the font-size property for both, but use the value 40px for the h1 and 30px for the h2.


h1 {
  font-size: 40px
}

h2 {
  font-size: 30px
}

 ```

## 63

```html

- Add a footer element below the main element, where you can add some additional information.

<footer> </footer>

 ```

## 64

```html
- Inside the footer, add a p element. Then, nest an anchor (a) element in the p that links to https://www.freecodecamp.org and has the text Visit our website.

<footer>
        <p> <a href="https://www.freecodecamp.org"> Visit our website </a> </p>
      </footer>
```

## 65

```html
- Add a second p element below the one with the link and give it the text 123 Free Code Camp Drive.

<p>
          <a href="https://www.freecodecamp.org" target="_blank">Visit our website</a>
        </p>
        <p> 123 Free Code Camp Drive</p>
```

## 66

```html
-added hr element to seperate content, it is a line on the page, it is also a void element

<hr>
```

## 67

```html
- The default properties of an hr element will make it appear as a thin light grey line. You can change the height of the line by specifying a value for the height property.

- Change the height of the hr element to be 3px.

hr {
  height: 3px;
}
```

## 68

```html

- changed hr background to match color of beans

hr {
  height: 3px;
  background-color: brown;
}
```

## 69

```html

- Notice the grey color along the edges of the line. Those edges are known as borders. Each side of an element can have a different color or they can all be the same.

- Make all the edges of the hr element the same color as the background of it using the border-color property.

hr {
  height: 3px;
  background-color: brown;
  border-color: brown;
}
```

## 70

```html

- changed height of hr element to 2px

hr {
  height: 2px;
  background-color: brown;
  border-color: brown;
}
```

## 71

```html

- added another hr element below main and above the footer to seperate it

<hr>>
```

## 72

```html

- To create a little more room around the menu, add 20px of space on the inside of the body element by using the padding property.

body {
  background-image: url(https://cdn.freecodecamp.org/curriculum/css-cafe/beans.jpg);
  font-family: sans-serif;
  padding: 20px;
}
```

## 73

```html

- Focusing on the menu items and prices, there is a fairly large gap between each line.

 - Use the existing selector that targets all the p elements nested in elements with the class named item and set their top and bottom margin to be 5px.

.item p {
  display: inline-block;
  margin-top: 5px;
  margin-bottom: 5px;

}
```

## 74

```html

- made font size of items and price 18px

.item p {
  display: inline-block;
  margin-top: 5px;
  margin-bottom: 5px;
  font-size: 18px;
}
```

## 75

```html

- Changing the margin-bottom to 5px looks great. However, now the space between the Cinnamon Roll menu item and the second hr element does not match the space between the top hr element and the Coffee heading.

 - Add some more space by creating a class named bottom-line using 25px for the margin-top property.

.bottom-line {
  margin-top: 25px;
}
```

## 76

```html

- Now add the bottom-line class to the second hr element so the styling is applied.

<hr class="bottom-line">
```

## 77

```html

- added comment to organize styles.css to seperate where we are styling the footer

/* FOOTER */

```

## 78

```html

- Moving down to the footer element, make all the text have a value of 14px for the font size.

footer {
  font-size: 14px;
}
```

## 79

```html

- The default color of a link that has not yet been clicked on is typically blue. The default color of a link that has already been visited from a page is typically purple.

- To make the footer links the same color regardless if a link has been visited, use a type selector for the anchor element (a) and use the value black for the color property.

a {
  color: black;
}
```

## 80

```html

- You change properties of a link when the link has actually been visited by using a pseudo-selector that looks like a:visited { propertyName: propertyValue; }.

- Change the color of the footer Visit our website link to be grey when a user has visited the link.

a:visited { 
  color: grey; 
  }
```

## 81

```html

- You change properties of a link when the mouse hovers over them by using a pseudo-selector that looks like a:hover { propertyName: propertyValue; }.

- Change the color of the footer Visit our website link to be brown when a user hovers over it.

a:hover { 
  color: brown; 
  }
```

## 82

```html

- You change properties of a link when the link is actually being clicked by using a pseudo-selector that looks like a:active { propertyName: propertyValue; }.

- Change the color of the footer Visit our website link to be white when clicked on.

a:active { 
  color: white; 
  }
```

## 83

```html

- To keep with the same color theme you have already been using (black and brown), change the color for when the link is visited to black and use brown for when the link is actually clicked.

a:visited {
  color: black;
}

a:hover {
  color: brown;
}

a:active {
  color: brown;
}
```

## 84

```html

- The menu text CAMPER CAFE has a different space from the top than the address's space at the bottom of the menu. This is due to the browser having some default top margin for the h1 element.

- Change the top margin of the h1 element to 0 to remove all the top margin.

h1 {
  font-size: 40px;
  margin-top: 0;
}
```

## 85

```html

- To remove some of the vertical space between the h1 element and the text Est. 2020, change the bottom margin of the h1 to 15px.

h1 {
  font-size: 40px;
  margin-top: 0;
  margin-bottom: 15px;
}
```

## 86

```html

- Now the top spacing looks good. The space below the address at the bottom of the menu is a little bigger than the space at the top of the menu and the h1 element.

- To decrease the default margin space below the address p element, create a class selector named address and use the value 5px for the margin-bottom property.

.address {
  margin-bottom: 5px;
}
```

## 87

```html

- Now apply the address class to the p element containing the street address 123 Free Code Camp Drive

<footer>
        <p>
          <a href="https://www.freecodecamp.org" target="_blank">Visit our website</a>
        </p>
        <p class="address">123 Free Code Camp Drive</p>
      </footer>
```

## 88

```html

- The menu looks good, but other than the coffee beans background image, it is mainly just text.

- Under the Coffee heading, add an image using the url https://cdn.freecodecamp.org/curriculum/css-cafe/coffee.jpg. Give the image an alt value of coffee icon.

<h2>Coffee</h2>
          <img src="https://cdn.freecodecamp.org/curriculum/css-cafe/coffee.jpg" alt="coffee icon">
```

## 89

```html

- The image you added is not centered horizontally like the Coffee heading above it. img elements are "like" inline elements.

- To make the image behave like heading elements (which are block-level), create an img type selector and use the value block for the display property and use the applicable margin-left and margin-right values to center it horizontally.

img {
  display: block;
  margin-left: auto;
  margin-right: auto;
}
```

## 90

```html

- Add one last image under the Desserts heading using the url https://cdn.freecodecamp.org/curriculum/css-cafe/pie.jpg. Give the image an alt value of pie icon.

<h2>Desserts</h2>
          <img src="https://cdn.freecodecamp.org/curriculum/css-cafe/pie.jpg" alt="pie icon">
```

## 91

```html

- It would be nice if the vertical space between the h2 elements and their associated icons was smaller. The h2 elements have default top and bottom margin space, so you could change the bottom margin of the h2 elements to say 0 or another number.

- There is an easier way, simply add a negative top margin to the img elements to pull them up from their current positions. Negative values are created using a - in front of the value. To complete this project, go ahead and use a negative top margin of 25px in the img type selector.

img {
  display: block;
  margin-left: auto;
  margin-right: auto;
  margin-top: -25px
}
```
