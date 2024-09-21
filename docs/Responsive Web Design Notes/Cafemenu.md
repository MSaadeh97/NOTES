# Cafe Menu

## 1. Tags

- CSS (Cascading Style Sheets) by building a cafe menu. CSS is the language used to style an HTML document. It describes how HTML elements should be displayed on the screen.
- Every HTML document should have a DOCTYPE declaration and html element. The DOCTYPE tells the browser which version of HTML the document is in. And the html element represents the root element which contains all other elements.

```html
<!DOCTYPE html>
<html lang="en">
<!--all other elements go here-->
</html>
```

## 2

```html
<head> 
    <title> Cafe Menu </title>
</head>
```

## 3

- The title is one of several elements that provide extra information not visible on the web page, but it is useful for search engines or how the page gets displayed.

- Inside the head element, nest a meta element with an attribute named charset set to the value utf-8 to tell the browser how to encode characters for the page.

```html
<head>
    <title>Cafe Menu</title>
    <meta charset="utf-8">
</head>
```

## 4

```html
<body>
</body>
```

## 5

```html
<body>
<main>
</main>
</body>
```

## 6

```html
<body>
<main>
    <h1> camper cafe </h1>
</main>
</body>
```

## 7

```html
<h1> camper cafe </h1>
<p> Est. 2020 <p>
```

## 8

```html

<main>
      <h1>CAMPER CAFE</h1>
      <p>Est. 2020</p>
      <section>
        </section>
    </main>
```

## 9

```html
<section>
    <h2> Coffee </h2>
</section>
```

## 10

- added a style element to the head element

```html
<style>
</style>
```

## 11

- You can add style to an element by specifying it in the style element and setting a property for it like this:

```html

h1 {
 text-align: center;
}

```

## 12

-In the previous step, you used a type selector to style the h1 element. Center the content of the h2 and the p elements by adding a new type selector for each one to the existing style element.

```html
p {
 text-align: center;
}

h2 {
 text-align: center;
}
```

## 13

- You now have three type selectors with the exact same styling. You can add the same group of styles to many elements by creating a list of selectors. Each selector is separated with commas like this:

p,h1,h2 {
 text-align: center;
}

- Delete the three existing type selectors and replace them with one selector list that centers the text for the h1, h2, and p elements.

## 14

- This works, but since there will be many more styles, it's best to put all the styles in a separate file and link to it.

## 15

- removed style content to later link the style sheet

## 16

- Inside the head element, add a link element. Give it a rel attribute with the value of "stylesheet" and a href attribute with the value of "styles.css".

```html
<link rel="stylesheet" href="styles.css">
```

## 17

- For the styling of the page to look similar on mobile as it does on a desktop or laptop, you need to add a meta element with a special content attribute.

- Add the following within the head element:

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
```

## 18

- Add another style to the file that changes the background-color property to brown for the body element.

```html
body {
  background-color: brown;
}
```

## 19

```html
body {
  background-color: burlywood;
}
```

## 20

- The div element is used mainly for design layout purposes unlike the other content elements you have used so far. Add a div element inside the body element and then move all the other elements inside the new div.

- Inside the opening div tag, add the id attribute with a value of menu.

```html
<div id="menu">
</div>
 ```

## 21

- You can use the id selector to target a specific element with an id attribute. An id selector is defined by placing the hash symbol # directly in front of the element's id value. For example, if an element has the id of cat then you would target that element like this:

- Example Code
- #cat {
  - width: 250px;
- }
- Use the #menu selector to give your element a width of 300px.

```html
#menu {
  width: 300px;
}
 ```

## 22

```html
/* background-color: burlywood; */
 ```

## 23

```html
#menu {
  background-color: burlywood;
  width: 300px;
}
 ```

## 24

- Now it's easy to see that the text is centered inside the #menu element. Currently, the width of the #menu element is specified in pixels (px).

- Change the width property's value to be 80%, to make it 80% the width of its parent element (body).

```html
#menu {
  width: 80%;
  background-color: burlywood;
}
 ```

## 25

- Next, you want to center the #menu horizontally. You can do this by setting its margin-left and margin-right properties to auto. Think of the margin as invisible space around an element. Using these two margin properties, center the #menu element within the body element.

```html
#menu {
  width: 80%;
  background-color: burlywood;
  margin-left: auto;
  margin-right: auto;
}
 ```

## 26

- So far you have been using type and id selectors to style elements. However, it is more common to use a different selector to style your elements.

A class selector is defined by a name with a dot directly in front of it, like this:

Example Code
.class-name {
  styles
}
Change the existing #menu selector into a class selector by replacing #menu with a class named .menu.

```html
.menu {
  width: 80%;
  background-color: burlywood;
  margin-left: auto;
  margin-right: auto;
}
 ```

## 27

- To apply the class's styling to the div element, remove the id attribute and add a class attribute to the div element's opening tag. Make sure to set the class value to menu.

```html
 <div class="menu">
 ```

## 28

```html
<!-- added an image in the body element -->
 body {
  background-image:url(https://cdn.freecodecamp.org/curriculum/css-cafe/beans.jpg);
}
```

## 29

- Time to start adding some menu items. Add an empty article element under the Coffee heading. It will contain a flavor and price of each coffee you currently offer.

```html
<article></article>
```

## 30

- article elements commonly contain multiple elements that have related information. In this case, it will contain a coffee flavor and a price for that flavor. Nest two p elements inside your article element. The first one's text should be French Vanilla, and the second's text 3.00.

```html
<article>
            <p> French Vanilla </p>
            <p> 3.00 </p>
          </article>
```

## 31

```html
<!-- added more articles to include more coffee price pairs -->
 <article>
            <p>French Vanilla</p>
            <p>3.00</p>
          </article>
          <article>
            <p>Caramel Macchiato</p>
            <p>3.75</p>
          </article>
          <article>
            <p>Pumpkin Spice</p>
            <p>3.50</p>
          </article>
          <article>
            <p>Hazelnut</p>
            <p>4.00</p>
          </article>
          <article>
            <p>Mocha</p>
            <p>4.50</p>
          </article>
```

## 32

```html
<!-- added class element to p tag to edit flavor to the left and price to the right -->
 <p class="flavor">French Vanilla</p>
            <p>3.00</p> 
```

## 33

```html
<!-- add class selector .flavor to text align flavor to the left -->
 .flavor {
  text-align: left;
}
```

## 34

```html
<!-- added class element to p tag with the price to add class selector and have text align to the right -->
 <p class="price">3.00</p>
```

## 35

```html
<!-- added .price class selector -->
 .price {
  text-align:right;
}
```

## 36

```html
<!-- start to inline both p tags so they are lined up on the same line in the menu as p tags are naturally block level elements -->
 <article class="item">
```

## 37

```html
<!-- The p elements are nested in an article element with the class attribute of item. You can style all the p elements nested anywhere in elements with a class named item like this: -->
 .item p {
  display: inline-block;
}
```

## 38

```html
<!-- That's closer, but the price didn't stay over on the right. This is because inline-block elements only take up the width of their content. To spread them out, add a width property to the flavor and price class selectors that have a value of 50% each. -->
 .flavor {
  width: 50%;
  text-align: left;
}

.price {
  width: 50%;
  text-align: right;
}
```

## 39

```html
<!--  Styling the p elements as inline-block and placing them on separate lines in the code creates an extra space to the right of the first p element, causing the second one to shift to the next line. One way to fix this is to make each p element's width a little less than 50%. -->
 .flavor {
  text-align: left;
  width: 49%;
}

.price {
  text-align: right;
  width: 49%;
}
```

## 40

```html
<!-- put the p elements on the same line in the editor -->
 <p class="flavor">French Vanilla</p><p class="price">3.00</p>
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
