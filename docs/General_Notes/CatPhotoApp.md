# Cat Photo APP

## 1. Tags

- HTML has opening and closing tags

```html
<h1> Hello world </h1>
```

## 2

```html
<h1> CatPhotoApp </h1>
```

## 3

```html
<h2> CatPhotoApp </h2>
```

## 4

```html
<--! TODO: Remove h1 -->
```

## 5

```html
<main>
</main>
```

## 6

```html
<h1> hello world</h1>
<p> Some more important content..nesting</p>
```

## 7

```html
<img>
```

## 8

```html
<img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/relaxing-cat.jpg">
```

## 9

```html
<img src="cat.jpg" alt="A cat">
```

## 10

```html
<a href="https://www.freecodecamp.org"></a>
```

## 11

```html
<a href="https://www.freecodecamp.org">click here to go to freeCodeCamp.org</a>
```

## 12

```html
<p>I think <a href="https://www.freecodecamp.org">freeCodeCamp</a> is great.</p>
```

## 13

<!-- Remember to try to simplify code if able such as creating a link in a phrase rather than needing a whole line -->

## 14

```html
<a href="https://www.freecodecamp.org" target="_blank">freeCodeCamp</a>
```

## 15

```html
<a href="example-link">
  <img src="image-link.jpg" alt="A photo of a cat.">
</a>
```

## 16

```html
<section>
</section>
```

## 17

```html
<!-- add new sections to organzie page elements -->
```

## 18

```html
<section>
<h2> Cat lists </h2>
</section>
```

## 19

```html
<!-- when using a lower heading element, it is implied you are starting a new subsection -->
```

## 20

```html
<!-- to create an unordered list, use the <ul> </ul> Tags -->
 ```

## 21

```html
<!-- to create a item in your unordered or ordered list, use <li> </li> Tags -->
 ```

## 22

```html
<img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/lasagna.jpg" alt="A slice   of lasagna on a plate.">
 ```

## 23

```html
<!-- The figure element represents self-contained content and will allow you to associate an image with a caption. -->

 <figure>

</figure>
 ```

## 24

```html
<figure>
          <img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/lasagna.jpg" alt="A slice of lasagna on a plate.">
          <figcaption> Cats love lasagna </figcaption>
        </figure>
 ```

## 25

```html
<!-- To place emphasis on a specific word or phrase, you can use the em element. -->
<figcaption>Cats <em>love</em> lasagna.</figcaption>
 ```

## 26

```html
<h3> Top 3 things cats hate: </h3>
 ```

## 27

```html
<!-- The code for an ordered list (ol) is similar to an unordered list, but list items in an ordered list are numbered when displayed. -->
 <ol>
            <li>flea treatment</li>
            <li>thunder</li>
            <li>other cats</li>
        </ol>
 ```

## 28

```html
<!-- added another figure elemet -->
```

## 29

```html
<!-- added nested img elemtn with src attribute in the figure element -->
```

## 30

```html
<!-- added a alt attribute to the img element -->
```

## 31

```html
<!-- added a fig caption after the img element -->
```

## 32

```html
<!-- The strong element is used to indicate that some text is of strong importance or urgent. -->
 <figcaption>Cats <strong>hate</strong> other cats.</figcaption> 
```

## 33

```html
<!-- added another section for our 3rd section -->
```

## 34

```html
<!-- added another h2 element in the 3rd section -->
```

## 35

```html
<!-- The form element is used to get information from a user like their name, email, and other details. -->
 <form> </form>
```

## 36

```html
<!-- The action attribute indicates where form data should be sent. -->
 <form action="https://freecatphotoapp.com/submit-cat-photo">
        </form>
```

## 37

```html
<!-- The input element allows you several ways to collect data from a web form. Like img elements, input elements are a void element and do not need closing tags. -->
 <input>
```

## 38

```html
<!-- added text to type attribute to allow user input -->
 <input type="text">
```

## 39

```html
<!-- In order for a form's data to be accessed by the location specified in the action attribute, you must give the text field a name attribute and assign it a value to represent the data being submitted. -->
 <input type="text" name="catphotourl">
```

## 40

```html
<!-- Placeholder text is used to give people a hint about what kind of information to enter into an input.

Here is an example of an input element with a placeholder set to Ex. Jane Doe: -->
 <input type="text" name="catphotourl" placeholder="cat photo URL">
```

## 41

```html
<!-- To prevent a user from submitting your form when required information is missing, you need to add the required attribute to an input element. There's no need to set a value to the required attribute. Instead, just add the word required to the input element, making sure there is space between it and other attributes. -->
 <input type="text" name="catphotourl" placeholder="cat photo URL" required="">
```

## 42

```html
<!-- The button element is used to create a clickable button. text between the button tags comes up on the button -->
 <button> Submit </button>
```

## 43

```html
<!-- Even though you added your button below the text input, they appear next to each other on the page. That's because both input and button elements are inline elements, which don't appear on new lines.

The button you added will submit the form by default. However, relying on default behavior may cause confusion. Add the type attribute with the value submit to the button to make it clear that it is a submit button. -->
 <button type="submit">Submit</button>
```

## 44

```html
<!-- You can use radio buttons for questions where you want only one answer out of multiple options.

Here is an example of a radio button with the option of cat:

Example Code
<input type="radio"> cat
Remember that an input element is a void element. -->
 <input type="radio"> Indoor
          <input type="text" name="catphotourl" placeholder="cat photo URL" required>
```

## 45

```html
<!-- label elements are used to help associate the text for an input element with the input element itself (especially for assistive technologies like screen readers).

Here is an example of a label element with a radio button:

Example Code
<label><input type="radio"> cat</label> -->
  <label><input type="radio"> Indoor </label>
```

## 46

```html
<!-- The id attribute is used to identify specific HTML elements. Each id attribute's value must be unique from all other id values for the entire page.

Here is an example of an input element with an id attribute:

Example Code
<input id="email"> -->
  <label><input type="radio" id="indoor"> Indoor</label>
```

## 47

```html
<!-- created another label radio as outdoor -->
  <label><input id="indoor" type="radio"> Indoor</label>
  <label><input id="outdoor" type="radio"> Outdoor</label>
```

## 48

```html

<!-- Notice that both radio buttons can be selected at the same time. To make it so selecting one radio button automatically deselects the other, both buttons must have a name attribute with the same value.

Here is an example of two radio buttons with the same name attribute:

Example Code
<input type="radio" name="meal"> Breakfast
<input type="radio" name="meal"> Lunch -->
  <label><input id="indoor" type="radio" name="indoor-outdoor"> Indoor</label>
          <label><input id="outdoor" type="radio" name="indoor-outdoor"> Outdoor</label>

```

## 49

```html

<!-- If you select the Indoor radio button and submit the form, the form data for the button is based on its name and value attributes. Since your radio buttons do not have a value attribute, the form data will include indoor-outdoor=on, which is not useful when you have multiple buttons.

Add a value attribute to both radio buttons. For convenience, set the button's value attribute to the same value as its id attribute. -->
  <label><input id="indoor" type="radio" name="indoor-outdoor" value="indoor"> Indoor</label>
          <label><input id="outdoor" type="radio" name="indoor-outdoor" value="outdoor"> Outdoor</label>

```

## 50

```html

<!-- The fieldset element is used to group related inputs and labels together in a web form. fieldset elements are block-level elements, meaning that they appear on a new line. -->
  <fieldset>
          <label><input id="indoor" type="radio" name="indoor-outdoor" value="indoor"> Indoor</label>
          <label><input id="outdoor" type="radio" name="indoor-outdoor" value="outdoor"> Outdoor</label>
        </fieldset>
          
```

## 51

```html

<!-- The legend element acts as a caption for the content in the fieldset element. It gives users context about what they should enter into that part of the form.

Add a legend element with the text Is your cat an indoor or outdoor cat? above both of the radio buttons. -->
  <fieldset>
            <legend> Is your cat an indoor or outdoor cat? </legend>
            <label><input id="indoor" type="radio" name="indoor-outdoor" value="indoor"> Indoor</label>
            <label><input id="outdoor" type="radio" name="indoor-outdoor" value="outdoor"> Outdoor</label>
          </fieldset>
          
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

```html
  <!-- added checked attribute after input tag to check radio and checkbox by default, only the first options -->
```

## 65

```html
  <!-- The head element is used to contain metadata about the document, such as its title, links to stylesheets, and scripts. Metadata is information about the page that isn't displayed directly on the page. located above the body element -->
```

## 66

```html
<!-- The head element is used to contain metadata about the document, such as its title, links to stylesheets, and scripts. Metadata is information about the page that isn't displayed directly on the page. located above the body element -->
```

## 67

```html
<!-- The title element determines what browsers show in the title bar or tab for the page. located inside the head element -->
```

## 68

```html

<!-- All pages should begin with <!DOCTYPE html>. This special string is known as a declaration and ensures the browser tries to meet industry-wide specifications.

<!DOCTYPE html> tells browsers that the document is an HTML5 document which is the latest version of HTML.

Add this declaration as the first line of the code. -->
```

## 69

```html

<!-- You can set browser behavior by adding meta elements in the head. Here's an example:

Example Code
<meta attribute="value">
Inside the head element, nest a meta element with an attribute named charset. Set to the value to utf-8 which tells the browser how to encode characters for the page.

Note that the meta element is a void element. -->
<meta charset="utf-8">
```
