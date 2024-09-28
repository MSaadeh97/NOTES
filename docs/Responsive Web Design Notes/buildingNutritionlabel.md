# Building Nutrition Label

## 1. Tags

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <title>Nutrition Label</title>
</head>

<body>
<h1>Nutrition Facts</h1>
</body>
</html>
```

## 2

- Below your h1 element, add a p element with the text 8 servings per container.

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <title>Nutrition Label</title>
</head>

<body>
  <h1>Nutrition Facts</h1>
    <p>8 servings per container</p>
</body>
</html>
```

## 3

- Add a second p element with the text Serving size 2/3 cup (55g).

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <title>Nutrition Label</title>
</head>

<body>
  <h1>Nutrition Facts</h1>
  <p>8 servings per container</p>
  <p>Serving size 2/3 cup (55g)</p>  
</body>
</html>
```

## 4

<!--  Within your head element, add a link element with the rel attribute set to stylesheet and the href attribute set to https://fonts.googleapis.com/css?family=Open+Sans:400,700,800. -->

- This will import the Open Sans font family, with the font weight values 400, 700, and 800.

- Also add a link element to link your styles.css file.

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <title>Nutrition Label</title>
  <link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Open+Sans:400,700,800">
  <link rel="stylesheet" href="styles.css">
</head>

<body>
  <h1>Nutrition Facts</h1>
  <p>8 servings per container</p>
  <p>Serving size 2/3 cup (55g)</p>
</body>
</html>
```

## 5

- Create a body selector and give it a font-family set to Open Sans with a fallback of sans-serif.

- Remember that fonts with spaces in the name must be wrapped in quotes for CSS. 

```html
body {
font-family: "Open Sans", sans-serif
}
```

## 6

- The font is a bit small. Create an html selector and set the font to have a size of 16px.

```html
html {
  font-size: 16px
}
```

## 7

- Wrap your h1 and p elements in a div element. Give that div a class attribute set to label.

```html
<body>
  <div class="label">
  <h1>Nutrition Facts</h1>
  <p>8 servings per container</p>
  <p>Serving size 2/3 cup (55g)</p>
  </div>
</body>
```

## 8

- Borders can be used to group and prioritize content.

- Create a .label selector and give it a border set to 2px solid black.

```html

.label {
  border: 2px solid black;
}
```

## 9

- Good use of white space can bring focus to the important elements of your page, and help guide your user's eyes through your text.

- Give your .label selector a width property set to 270px.

```html
.label {
  border: 2px solid black;
  width: 270px;
}
```

## 10

- Give your .label selector a margin property set to 20px auto, and a padding property set to 0 7px.

```html
.label {
  border: 2px solid black;
  width: 270px;
  margin: 20px auto;
  padding: 0 7px;
}
```

## 11

- If you inspect your .label element with your browser's developer tools, you may notice that it's actually 288 pixels wide instead of 270. This is because, by default, the browser includes the border and padding when determining an element's size.

- To solve this, reset the box model by creating a * selector and giving it a box-sizing property of border-box.

```html

* {
  box-sizing: border-box;
}

```

## 12

- Remember that the use of h1, h2, and similar tags determine the semantic structure of your HTML. However, you can adjust the CSS of these elements to control the visual flow and hierarchy.

- Create an h1 rule and set the font-weight property to 800. This will make your h1 text bolder.

```html
h1 {
  font-weight: 800;
}
```

## 13

- Give your h1 selector a text-align property of center.

```html
h1 {
  font-weight: 800;
  text-align: center;
}
```

## 14

- Fine-tune the placement of your h1 by giving it a top and bottom margin of -4px and a left and right margin of 0.

h1 {
  font-weight: 800;
  text-align: center;
  margin: -4px 0;
}

## 15

- Create a p selector and remove all margins.

p {
  margin: 0
  }

## 16

- Lines can help separate and group important content, especially when space is limited.

- Create a div element below your h1 element, and give it a class attribute set to divider.

```html
<div class="label">
    <h1>Nutrition Facts</h1>
    <div class="divider"> </div>
    <p>8 servings per container</p>
    <p>Serving size 2/3 cup (55g)</p>
  </div>
```

## 17

- Create a selector for your new .divider and set the border-bottom property to 1px solid #888989. Also give it a top and bottom margin of 2px. It should not have any left or right margin.

```html
.divider {
  border-bottom: 1px solid #888989;
  margin: 2px 0;
}
```

## 18

- The letter-spacing property can be used to adjust the space between each character of text in an element.

- Give your h1 selector a letter-spacing property set to 0.15px to space them out a bit more.

```html
h1 {
  font-weight: 800;
  text-align: center;
  margin: -4px 0;
  letter-spacing: 0.15px;
}
```

## 19

- Nutrition labels have a lot of bold text to draw attention to important information. Rather than targeting each element that needs to be bold, it is more efficient to use a class to apply the bold styling to every element.

- Give your second p element a class attribute set to bold.

```html
<div class="label">
    <h1>Nutrition Facts</h1>
    <div class="divider"></div>
    <p>8 servings per container</p>
    <p class="bold">Serving size 2/3 cup (55g)</p>
  </div>
```

## 20

- Your new class does not have any styling yet. Create a .bold selector and give it a font-weight property set to 800 to make the text bold.

- Go ahead and remove the font-weight property from your h1 selector as well.

```html
h1 {
  text-align: center;
  margin: -4px 0;
  letter-spacing: 0.15px;
}

p {
  margin: 0;
}

.divider {
  border-bottom: 1px solid #888989;
  margin: 2px 0;
}

.bold {
  font-weight: 800;
}
 ```

## 21

- Give your h1 element a class attribute set to bold. This will make the text bold again.

```html
<div class="label">
    <h1 class="bold">Nutrition Facts</h1>
    <div class="divider"></div>
    <p>8 servings per container</p>
    <p class="bold">Serving size 2/3 cup (55g)</p>
  </div>
 ```

## 22

- Horizontal spacing between equally important elements can increase the readability of your text.

- Wrap the text 2/3 cup (55g) in a span element.

```html
<div class="label">
    <h1 class="bold">Nutrition Facts</h1>
    <div class="divider"></div>
    <p>8 servings per container</p>
    <p class="bold">Serving size <span>2/3 cup (55g)</span></p>
  </div>
 ```

## 23

- Now we can add the horizontal spacing using flex. In your p selector, add a display property set to flex and a justify-content property set to space-between.

```html
p {
  margin: 0;
  display: flex;
  justify-content: space-between;
}
 ```

## 24

- Wrap everything within the .label element in a new header element.

```html
<body>
  <div class="label">
    <header>
    <h1 class="bold">Nutrition Facts</h1>
    <div class="divider"></div>
    <p>8 servings per container</p>
    <p class="bold">Serving size <span>2/3 cup (55g)</span></p>
    </header>
  </div>
 ```

## 25

- Now update your h1 selector to be header h1 to specifically target your h1 element within your new header.

```html
header h1 {
  text-align: center;
  margin: -4px 0;
  letter-spacing: 0.15px
}
 ```

## 26

- Create a new div element below your header element, and give it a class attribute set to divider large.

```html
<div class="divider large"></div>
 ```

## 27

- Create a new .large selector and give it a height property set to 10px. Also create an .large, .medium selector and set the background-color property to black.

```html
 .large {
  height: 10px;
  background-color: black;
}

.large, .medium {
  background-color: black;
}
 ```

## 28

- You may notice there is still a small border at the bottom of your .large element. To reset this, give your .large, .medium selector a border property set to 0.

- Note: the medium(medium) class will be utilized later for the thinner bars of the nutrition label.

```html
.large, .medium {
  background-color: black;
  border: 0;
}
```

## 29

- Create a new div below your .large element and give it a class attribute set to calories-info.

```html
<div class="calories-info"></div>
```

## 30

- Within your .calories-info element, create a div element. Give that div element a class attribute set to left-container. Within the newly created div element, create a h2 element with the text Amount per serving. Give the h2 element a class attribute set to bold small-text.

```html
<div class="calories-info">
      <div class="left-container">
        <h2 class="bold small-text">Amount per serving</h2>
        </div>
    </div>
```

## 31

- The rem unit stands for root em, and is relative to the font size of the html element.

- Create a .small-text selector and set the font-size to 0.85rem, which would calculate to roughly 13.6px (remember that you set your html to have a font-size of 16px).

```html
.small-text {
  font-size: 0.85rem;
}
```

## 32

- Create a .calories-info h2 selector and remove all margins.

```html
.calories-info h2 {
  margin: 0;
}
```

## 33

- Below your .small-text element, create a new p element with the text Calories. Also below the .left-container element, create a new span element with the text 230.

```html
<div class="calories-info">
      <div class="left-container">
        <h2 class="bold small-text">Amount per serving</h2>
        <p>Calories</p>
      </div>
      <span>230</span>
    </div>
```

## 34

- Create a new .calories-info selector and give it a display property set to flex. Also give it a justify-content property set to space-between and align-items property set to flex-end.

```html
.calories-info {
  display: flex;
  justify-content: space-between;
  align-items: flex-end;
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
