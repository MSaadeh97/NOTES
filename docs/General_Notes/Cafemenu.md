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

<!-- added a new fieldset element under the first one to add a new form -->
          
```

## 53

```html

<!-- added a legend in the field set with text --> 
          
```

## 54

```html

<!-- Forms commonly use checkboxes for questions that may have more than one answer. The input element with a type attribute set to checkbox creates a checkbox. --> 
          <input type="checkbox"> Loving
```

## 55

```html

<!-- added id attribute loving -->

```

## 56

```html

<!-- There's another way to associate an input element's text with the element itself. You can nest the text within a label element and add a for attribute with the same value as the input element's id attribute.

Given an input element as below:

Example Code
<input id="breakfast" type="radio" name="meal" value="breakfast">
An example of a label element that is associated to this input element is:

Example Code
<label for="breakfast">Breakfast</label> -->
 
<input id="loving" type="checkbox"> <label for="loving">Loving</label>

```

## 57

```html

<!-- added attribute name to input tag with value personality -->

```

## 58

```html

<!-- added another input tag for a new checkbox for lazy, with the same name value personality but different id and for attribute values -->

```

## 59

```html

<!-- added another checkboc for energetic -->

 ```

## 60

```html

<!-- added value attribute to each checkbox input element with its respective id value -->

 ```

## 61

```html

<!-- added checked attribute after input tag to check radio and checkbox by default, only the first options -->

<input checked id="loving" type="checkbox" name="personality" value="loving"> <label for="loving">Loving</label>

 ```

## 62

```html

<footer></footer>

 ```

## 63

```html

<footer>
      <p> No Copyright - freeCodeCamp.org </p>
    </footer>

 ```

## 64

## 65

## 66

## 67

## 68

## 69

## 70

## 71

## 72

## 73

## 74

## 75

## 76

## 77

## 78

## 79

## 80

## 81

## 82

## 83

## 84

## 85

## 86

## 87

## 88

## 89

## 90

## 91
