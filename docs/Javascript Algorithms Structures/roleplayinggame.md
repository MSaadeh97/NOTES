# Building role playing game

## 1. Tags

- JavaScript is a powerful language which allows you to build websites that are interactive.

Note: For all remaining projects in this curriculum, you will need a basic level of knowledge in HTML and CSS. If you are new to HTML and CSS, please go through the Responsive Web Design Certification.

To get started, create your standard HTML boilerplate with a DOCTYPE, html, head, and body, then add a meta tag for the charset. Add a title element and use the text RPG - Dragon Repeller for it. Include a link tag for your stylesheet to link the styles.css file.

Finally, create a div element with id set to game within your body.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>RPG - Dragon Repeller</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div id="game"></div>
</body>
</html>
```

## 2

- Now you can start writing your JavaScript. Begin by creating a script element. This element is used to load JavaScript into your HTML file.

Example Code
  // JavaScript code goes here
</script>

```html
<script>

  </script>
```

## 3

- One of the most powerful tools is your developer console. Depending on your browser, this might be opened by pressing F12 or Ctrl+Shift+I. On Mac, you can press Option + ⌘ + C and select "Console". You can also click the "Console" button above the preview window to see our built-in console.

The developer console will include errors that are produced by your code, but you can also use it to see values of variables in your code, which is helpful for debugging.

Add a console.log("Hello World"); line between your script tags. Then click the "Console" button to open the console. You should see the text "Hello World".

```html
<script>
      console.log("Hello World");
    </script>
```

## 4

- Before you start writing your project code, you should move it to its own file to keep things organized.

Remove your console.log("Hello World"); line. Then give your now empty script element a src attribute set to ./script.js.

```html
<script src="./script.js">
      
    </script>
```

## 5

- Your view has been switched to your new script.js file. Remember that you can use the tabs above to switch between files.

Add your console.log("Hello World"); line to this file, and see it appear in your console.

```html
console.log("Hello World");
```

## 6

- Remove your console.log("Hello World"); line to begin writing your project code.

In the previous project, you learned how to work with variables and the let keyword like this:

Example Code
let camperbot;
You also learned how to initialize a variable with a value like this:

Example Code
let age = 32;
Use the let keyword to declare a variable called xp and assign it the value of 0, a number.

```html
let xp = 0;
```

## 7

- Initialize another variable called health with a value of 100, and a variable called gold with a value of 50.

```html
let xp = 0;
let health = 100;
let gold = 50;
```

## 8

- Create another variable called currentWeaponIndex and set it to 0.

```html
let xp = 0;
let health = 100;
let gold = 50;
let currentWeaponIndex = 0;
```

## 9

- Declare a variable called fighting but do not initialize it with a value.

```html
let xp = 0;
let health = 100;
let gold = 50;
let currentWeaponIndex = 0;
let fighting;
```

## 10

- Declare two more variables named monsterHealth and inventory.

For your inventory variable, assign it the value of an array containing the string "stick".

Remember that you worked with arrays in the previous project like this:

Example Code
let exampleArray = ["first", "second", "third"];

```html
let xp = 0;
let health = 100;
let gold = 50;
let currentWeaponIndex = 0;
let fighting;
let monsterHealth;
let inventory = ["stick"];
```

## 11

- In your role playing game, users will be able to track their stats, buy weapons, and fight monsters. Before you can continue with the interactive JavaScript portion of the game, you need to first create the HTML elements that will display the game information.

Create four div elements within your #game element. Give them the following respective id values, in order: stats, controls, monsterStats, and text.

```html
<body>
    <div id="game">
      <div id="stats"></div>
      <div id="controls"></div>
      <div id="monsterStats"></div>
      <div id="text"></div>
    </div>
  </body>
```

## 12

- Create three span elements within your #stats element. Give each of them the class stat. Then give the first one the text XP: 0, the second one the text Health: 100, and the third one the text Gold: 50.

```html
<body>
    <div id="game">
      <div id="stats">
        <span class="stat">XP: 0</span>
        <span class="stat">Health: 100</span>
        <span class="stat">Gold: 50</span>
      </div>
      <div id="controls"></div>
      <div id="monsterStats"></div>
      <div id="text"></div>
    </div>
  </body>
```

## 13

- Wrap the numbers 0, 100, and 50 in span elements, and wrap those new span elements in strong elements. Then give your new span elements id values of xpText, healthText, and goldText, respectively.

Your answer should follow this basic structure:

Example Code

```html
<span class="stat">XP: <strong><span id="xpText">0</span></strong></span>
        <span class="stat">Health: <strong><span id="healthText">100</strong></span></span>
        <span class="stat">Gold: <strong><span id="goldText">50</strong></span></span>
```

## 14

- For your #controls element, create three button elements. The first should have the id set to button1, and the text Go to store. The second should have the id set to button2, and the text Go to cave. The third should have the id set to button3, and the text Fight dragon.

```html
<div id="controls">
        <button id="button1">Go to store</button>
        <button id="button2">Go to cave</button>
        <button id="button3">Fight dragon</button>
      </div>
```

## 15

- JavaScript interacts with the HTML using the Document Object Model, or DOM. The DOM is a tree of objects that represents the HTML. You can access the HTML using the document object, which represents your entire HTML document.

One method for finding specific elements in your HTML is using the querySelector() method. The querySelector() method takes a CSS selector as an argument and returns the first element that matches that selector. For example, to find the element in your HTML, you would write:

Example Code
let h1 = document.querySelector("h1");
Note that h1 is a string and matches the CSS selector you would use.

Create a button1 variable and use querySelector() to assign it your element with the id of button1. Remember that CSS id selectors are prefixed with a #.

```html
let button1 = document.querySelector("#button1");
```

## 16

- We have run into a slight problem. You are trying to query your page for a button element, but your script tag is in the head of your HTML. This means your code runs before the browser has finished reading the HTML, and your document.querySelector() will not see the button - because the browser hasn't processed it yet.

To fix this, move your script element out of the head element, and place it at the end of your body element (just before the closing </body> tag.)

```html
 <head>
    <meta charset="utf-8">
    <link rel="stylesheet" href="./styles.css">
    <title>RPG - Dragon Repeller</title>
  </head>
  <body>
    <div id="game">
      <div id="stats">
        <span class="stat">XP: <strong><span id="xpText">0</span></strong></span>
        <span class="stat">Health: <strong><span id="healthText">100</span></strong></span>
        <span class="stat">Gold: <strong><span id="goldText">50</span></strong></span>
      </div>
      <div id="controls">
        <button id="button1">Go to store</button>
        <button id="button2">Go to cave</button>
        <button id="button3">Fight dragon</button>
      </div>
      <div id="monsterStats"></div>
      <div id="text"></div>
    </div>
    <script src="./script.js"></script>
  </body>
```

## 17

- button1 is a variable that is not going to be reassigned. If you are not going to assign a new value to a variable, it is best practice to use the const keyword to declare it instead of the let keyword. This will tell JavaScript to throw an error if you accidentally reassign it.

Change your button1 variable to be declared with the const keyword.

```html
const button1 = document.querySelector("#button1");
```

## 18

- Use querySelector() to get the other two button elements using their ids: button2 and button3. Store them in variables called button2 and button3. Remember to use const.

```html
const button1 = document.querySelector("#button1");
const button2 = document.querySelector("#button2");
const button3 = document.querySelector("#button3");
```

## 19

- Similar to your #stats element, your #monsterStats element needs two span elements. Give them the class stat and give the first element the text Monster Name:  and the second the text Health: . After the text in each, add a strong element with an empty nested span element. Give the first inner span element an id of monsterName and the second inner span element an id of monsterHealth.

```html
<div id="monsterStats">
         <span class="stat">Monster Name: <strong><span id="monsterName"></span></strong></span>
            <span class="stat">Health: <strong><span id="monsterHealth"></span></strong></span>
      </div>
```

## 20

- Give your #text element the following text:

Example Code
Welcome to Dragon Repeller. You must defeat the dragon that is preventing people from leaving the town. You are in the town square. Where do you want to go? Use the buttons above.

```html
<div id="text">
        <p>Welcome to Dragon Repeller. You must defeat the dragon that is preventing people from leaving the town. You are in the town square. Where do you want to go? Use the buttons above.</p>
      </div>
 ```

## 21

- Now we need some quick styling. Start by giving the body a background-color set to #0a0a23.

```html
body {
  background-color: #0a0a23;
}
 ```

## 22

- Give the #text element a background-color of #0a0a23, a color of #ffffff, and 10px of padding on all sides.

```html
#text {
  background-color: #0a0a23;
  color: #ffffff;
  padding: 10px;
}
 ```

## 23

- Give your #game a maximum width of 500px and a maximum height of 400px. Set the background-color to #ffffff and the color to #ffffff.

Use margins to center it by setting the top margin to 30px, bottom margin to 0px, and the left and right margin to auto.

Finally, give it 10px of padding on all four sides.

```html
#game {
  max-width: 500px;
  max-height: 400px;
  background-color: #ffffff;
  color: #ffffff;
  margin-top: 30px;
  margin-bottom: 0px;
  margin-left: auto;
  margin-right: auto;
  padding: 10px;
}
 ```

## 24

- Using a selector list (selector1, selector2) give both your #controls and #stats elements a border of 1px solid #0a0a23, a #0a0a23 text color, and 5px of padding.

```html
#controls, #stats {
  border: 1px solid #0a0a23;
  padding: 5px;
  color: #0a0a23;
}
 ```

## 25

- Give your #monsterStats element the same border and padding as your #stats element. Set its color to #ffffff and give it a #c70d0d background.

```html
#monsterStats {
  border: 1px solid #0a0a23;
  background-color: #c70d0d;
  padding: 5px;
  color: #ffffff;
}
 ```

## 26

- For now, hide your #monsterStats element with the display property. Do not change any of the other styling.

```html
#monsterStats {
  display: none;
  border: 1px solid #0a0a23;
  padding: 5px;
  color: #ffffff;
  background-color: #c70d0d;
}
 ```

## 27

- Next, give your .stat elements a padding-right of 10px.

```html
.stat {
  padding-right: 10px;
}
 ```

## 28

- Finally, you will need to add some styles for your buttons. Start by setting the cursor property to pointer. Then set the text color to #0a0a23 and the background-color to #feac32.

Then set the background-image property to linear-gradient(#fecc4c, #ffac33). Lastly, set the border to 3px solid #feac32.

```html
button {
  cursor: pointer;
  color: #0a0a23;
  background-color: #feac32;
  background-image: linear-gradient(#fecc4c, #ffac33);
  border: 3px solid #feac32;
}
```

## 29

- Just like you did with the buttons, create variables for the following ids and use querySelector() to give them the element as a value:

text, xpText, healthText, goldText, monsterStats, and monsterName.

Remember to declare these with the const keyword, and name the variables to match the ids.

```html
const button1 = document.querySelector("#button1");
const button2 = document.querySelector("#button2");
const button3 = document.querySelector("#button3");
const text = document.querySelector("#text");
const xpText = document.querySelector("#xpText");
const healthText = document.querySelector("#healthText");
const goldText = document.querySelector("#goldText");
const monsterStats = document.querySelector("#monsterStats");
const monsterName = document.querySelector("#monsterName");
```

## 30

- Finally, use querySelector() to get the #monsterHealth element. Because you have already declared a monsterHealth variable earlier, you need to use a different variable name for this element.

Declare a new variable with the const keyword and name it monsterHealthText.

```html
const button1 = document.querySelector("#button1");
const button2 = document.querySelector("#button2");
const button3 = document.querySelector("#button3");
const text = document.querySelector("#text");
const xpText = document.querySelector("#xpText");
const healthText = document.querySelector("#healthText");
const goldText = document.querySelector("#goldText");
const monsterStats = document.querySelector("#monsterStats");
const monsterName = document.querySelector("#monsterName");
const monsterHealthText = document.querySelector("#monsterHealth");
```

## 31

- In the previous project, you learned how to create a function like this:

Example Code
function functionName() {

}
Create an empty function named goStore.

```html
function goStore() {

}
```

## 32

- For now, make your goStore function output the message "Going to store." to the console.

```html
function goStore() {
  console.log("Going to store.");
}
```

## 33

- Now create a goCave function that prints "Going to cave." to the console.

```html
"Going to cave.
```

## 34

- Now create a fightDragon function that prints "Fighting dragon." to the console.

```html
function fightDragon() {
  console.log("Fighting dragon.");
}
```

## 35

- In the previous project, you learned how to work with single line and multi-line comments like this:

Example Code
// I am a single-line comment

/*
  I am a multi-line comment
*/
Add a single-line comment that says initialize buttons.

```html
// initialize buttons
```

## 36

- button1 represents your first button element. These elements have a special property called onclick, which you can use to determine what happens when someone clicks that button.

You can access properties in JavaScript a couple of different ways. The first is with dot notation. Here is an example of using dot notation to set the onclick property of a button to a function reference.

Example Code
button.onclick = myFunction;
In this example, button is the button element, and myFunction is a reference to a function. When the button is clicked, myFunction will be called.

Use dot notation to set the onclick property of your button1 to the function reference of goStore. Note that button1 is already declared, so you don't need to use let or const.

```html
button1.onclick = goStore;
```

## 37

- Using the same syntax, set the onclick properties of button2 and button3 to goCave and fightDragon respectively.

Once you have done that, open your console and try clicking the buttons on your project.

```html
// initialize buttons
button1.onclick = goStore;
button2.onclick = goCave;
button3.onclick = fightDragon;
```

## 38

- The innerText property controls the text that appears in an HTML element. For example:

Example Code
The following example would change the text of the p element from Demo content to Hello World.

When a player clicks your Go to store button, you want to change the buttons and text. Remove the code inside the goStore function and add a line that updates the text of button1 to say "Buy 10 health (10 gold)".

```html
function goStore() {
  button1.innerText = "Buy 10 health (10 gold)";
}
```

## 39

- Now, add a line that updates the text of button2 to say "Buy weapon (30 gold)" and update the text of button3 to say "Go to town square".

```html
function goStore() {
  button1.innerText = "Buy 10 health (10 gold)";
  button2.innerText = "Buy weapon (30 gold)";
  button3.innerText = "Go to town square";
}
```

## 40

- You will also need to update the functions that run when the buttons are clicked again.

In your goStore() function, update the onclick property for each button to run buyHealth, buyWeapon, and goTown, respectively.

```html
console.log(result);
```

## 41

- Now you need to modify your display text. Change the innerText property of the text variable to be "You enter the store.".

```html
function goStore() {
  button1.innerText = "Buy 10 health (10 gold)";
  button2.innerText = "Buy weapon (30 gold)";
  button3.innerText = "Go to town square";
  button1.onclick = buyHealth;
  button2.onclick = buyWeapon;
  button3.onclick = goTown;
  text.innerText = "You enter the store.";
}
```

## 42

- Create three new empty functions called buyHealth, buyWeapon, and goTown.

```html
function buyHealth() {

}

function buyWeapon() {
  
}

function goTown() {
  
}
```

## 43

- Move your goTown function above your goStore function. Then copy and paste the contents of the goStore function into the goTown function.

```html
function goTown() {
button1.innerText = "Buy 10 health (10 gold)";
  button2.innerText = "Buy weapon (30 gold)";
  button3.innerText = "Go to town square";
  button1.onclick = buyHealth;
  button2.onclick = buyWeapon;
  button3.onclick = goTown;
  text.innerText = "You enter the store.";
}

function goStore() {
  button1.innerText = "Buy 10 health (10 gold)";
  button2.innerText = "Buy weapon (30 gold)";
  button3.innerText = "Go to town square";
  button1.onclick = buyHealth;
  button2.onclick = buyWeapon;
  button3.onclick = goTown;
  text.innerText = "You enter the store.";
}

function goCave() {
  console.log("Going to cave.");
}

function fightDragon() {
  console.log("Fighting dragon.");
}

function buyHealth() {

}

function buyWeapon() {

}
```

## 44

- In your goTown function, change your button elements' innerText properties to be "Go to store", "Go to cave", and "Fight dragon". Update your onclick properties to be goStore, goCave, and fightDragon, respectively.

Finally, update innerText property of your text to be "You are in the town square. You see a sign that says Store.".

```html
function goTown() {
  button1.innerText = "Go to store";
  button2.innerText = "Go to cave";
  button3.innerText = "Fight dragon";
  button1.onclick = goStore;
  button2.onclick = goCave;
  button3.onclick = fightDragon;
  text.innerText = "You are in the town square. You see a sign that says Store.";
}
```

## 45

- You need to wrap the text Store in double quotes. Because your string is already wrapped in double quotes, you'll need to escape the quotes around Store. You can escape them with a backslash \. Here is an example:

Example Code
const escapedString = "Naomi likes to play \"Zelda\" sometimes.";
Wrap the text Store in double quotes within your text.innerText line.

```html
function goTown() {
  button1.innerText = "Go to store";
  button2.innerText = "Go to cave";
  button3.innerText = "Fight dragon";
  button1.onclick = goStore;
  button2.onclick = goCave;
  button3.onclick = fightDragon;
  text.innerText = "You are in the town square. You see a sign that says \"Store\".";
}
```

## 46

- You have repetition in the goTown and goStore functions. Repetition in your code is a sign that you need another function.

In the previous project, you learned how to work with function parameters like this:

Example Code
function myFunction(param) {
  console.log(param);
}
Function parameters act as placeholders for values that you pass to the function when you call it.

Create an empty update function that takes a parameter called location.

```html
function update(location) {

}
```

## 47

- In your role playing game, you will be able to visit different locations like the store, the cave, and the town square. You will need to create a data structure that will hold the different locations.

Use const to create a variable called locations and assign it an empty array.

```html
const locations = [];
```

## 48

- Before you can begin to build out your locations array, you will first need to learn about objects. Objects are an important data type in JavaScript. The next few steps will be dedicated to learning about them so you will better understand how to apply them in your project.

Objects are non primitive data types that store key-value pairs. Non primitive data types are mutable data types that are not undefined, null, boolean, number, string, or symbol. Mutable means that the data can be changed after it is created.

Here is the basic syntax for an object:

Example Code
{
  key: value
}
You will learn about keys and values in the next few steps.

For now, create a const variable called cat and assign it an empty object {}.

Below that cat variable, add a console.log(cat) statement to see the object in the console.

```html
const cat = {}; 
console.log(cat);
```

## 49

- Objects are similar to arrays, except that instead of using indexes to access and modify their data, you access the data in objects through properties.

Properties consist of a key and a value. The key is the name of the property, and the value is the data stored in the property.

Here is an example of an object with a single property:

Example Code
const obj = {
  name: "Quincy Larson"
};
Inside your cat object, add a new property. The key should be name and the value should be the string "Whiskers".

Open up the console to see the updates to your object.

```html
const cat = {
  name: "Whiskers"
};
```

## 50

- If the property name (key) of an object has a space in it, you will need to use single or double quotes around the name.

Here is an example of an object with a property name that has a space:

Example Code
const spaceObj = {
  "Space Name": "Kirk",
};
If you tried to write a key without the quotes, it would throw an error:

Example Code
const spaceObj = {
  // Throws an error
  Space Name: "Kirk",
};

Add a new property with a key of "Number of legs" and value of 4 to the cat object.

Open up the console to see the output.

```html
const cat = {
  name: "Whiskers",
  "Number of legs": 4
};
```

## 51

- There are two ways to access the properties of an object: dot notation (.) and bracket notation ([]), similar to an array.

Dot notation is what you use when you know the name of the property you're trying to access ahead of time.

Example Code
object.property;
Here is a sample of using dot notation (.) to read the name property of the developer object:

Example Code
const developer = {
  name: "Jessica",
}

// Output: Jessica
console.log(developer.name);
Update your console statement to access the name property of the cat object using dot notation.

Open up the console to see the name of "Whiskers" logged to the console.

```html
console.log(cat.name)
          
```

## 52

- The second way to access the properties of an object is bracket notation ([]). If the property of the object you are trying to access has a space in its name, you will need to use bracket notation.

Example Code
objectName["property name"];
Here is a sample of using bracket notation to read an object's property:

Example Code
const spaceObj = {
  "Space Name": "Kirk",
};

spaceObj["Space Name"]; // "Kirk"
Update your console statement to use bracket notation to access the property "Number of legs" of the cat object.

Open up the console to see the output.

```html
console.log(cat["Number of legs"]);  
```

## 53

- Later on in the curriculum, you will dive deeper into objects. But for now, it is time to apply what you have learned to your role playing game.

Start by deleting your cat object and console statement.

```html

```

## 54

- Your locations array will hold different locations like the store, the cave, and the town square. Each location will be represented as an object.

Inside your locations array, add an object. Inside that object add a key called name with a value of "town square".

Remember to follow this syntax:

Example Code
{
  key: value
}

```html
const locations = [
  {
        name: "town square"
    }
];
```

## 55

- Just like array values, object properties are separated by a comma. Add a comma after your name property and add a button text property with the value of an empty array.

Since the property name has a space in it, you will need to surround it with quotes.

Example Code
{
  name: "Naomi",
  "favorite color": "purple"
}

```html
const sum = addTwoNumbers(5,10);
function addTwoNumbers(a , b) {
return a + b;
}
console.log(sum);

```

## 56

- With that quick review complete, you should remove your addTwoNumbers function, sum variable, and log statement.

```html


```

## 57

- Variables in JavaScript are available in a specific scope. In other words, where a variable is declared determines where in your code it can be used.

The first scope is the global scope. Variables that are declared outside of any "block" like a function or for loop are in the global scope. Your character, count, and rows variables are all in the global scope.

When a variable is in the global scope, a function can access it in its definition. Here is an example of a function using a global title variable:

Example Code
const title = "Professor ";
function demo(name) {
  return title + name;
}
demo("Naomi")
This example would return "Professor Naomi". Update your padRow function to return the value of concatenating your character variable to the beginning of the name parameter.

```html
function padRow(name) {
  return character + name;
}
```

## 58

- Variables can also be declared inside a function. These variables are considered to be in the local scope, or block scope. A variable declared inside a function can only be used inside that function. If you try to access it outside of the function, you get a reference error.

To see this in action, use const to declare a test variable in your padRow function. Initialise it with the value "Testing".

Then, below your function, try to log test to the console. You will see an error because it is not defined outside of the function's local scope. Remove that console.log to pass the tests and continue.

```html
function padRow(name) {
  const test = "Testing";
  return character + name;
}

```

## 59

- Values returned out of a function are used by calling the function. You can use the function call directly as the value it returns, or capture the returned value in a variable. This way, you can use the value assigned to a locally scoped variable, outside the function it was created in.

Example Code
function getName() {
  const name = "Camper cat";
  return name;
}

console.log(getName()); // "Camper cat"

const capturedReturnValue = getName();
console.log(capturedReturnValue); // "Camper cat"

console.log(name); // reference error
To use your "Testing" value, return it out of the padRow function by updating your return statement to return only the test variable.

```html
function padRow(name) {
  const test = "Testing";  
  return test;
}
 ```

## 60

- Below the return statement, log the string "This works!" to the console.

After doing that, you will see that the string "This works!" does not display in the console, and the console.log("This works!") line is greyed out.

Copy the console log and paste it above the return statement. Now, the string "This works!" should appear in the console.

An important thing to know about the return keyword is that it does not just define a value to be returned from your function, it also stops the execution of your code inside a function or a block statement. This means any code after a return statement will not run.

```html
function padRow(name) {
  const test = "Testing";
  console.log("This works!");
  return test;
  console.log("This works!")
}
 ```

## 61

- Now your call variable has the value "Testing". But your function is no longer using the name parameter.

Remove the name parameter from your function declaration, then remove your "CamperChan" string from the padRow call.

Also, remove both console.log from the padRow function.

```html
function padRow() {
  const test = "Testing";
  return test;
}
const call = padRow();
console.log(call);
 ```

## 62

- Because your function was no longer using the parameter, changing the argument did not affect it.

Go ahead and remove the test declaration and return statement from your padRow function, so the function is empty again.

```html
function padRow() {

}
const call = padRow();
console.log(call);
 ```

## 63

- As expected, your function now returns undefined again. Your call variable is not necessary any more, so remove the call declaration and the console.log for the call variable.

```html
function padRow() {

}

 ```

## 64

- In order to know how to format a row, your padRow function will need to know which row number you are on, and how many rows in total are being generated.

The best way to do this is by creating function parameters for them. Give your padRow function a rowNumber and rowCount parameter. Multiple parameters are separated by a comma:

Example Code
function name(first, second) {

}

```html
function padRow(rowNumber, rowCount) {

}
```

## 65

- Remember in an earlier step, you learned about return values. A function can return a value for your application to consume separately.

In a function, the return keyword is used to specify a return value. For example, this function would return the value given to the first parameter:

Example Code
function name(parameter) {
  return parameter;
}
Use the return keyword to return the value of the character variable, repeated rowNumber times.

```html
function padRow(rowNumber, rowCount) {
  return character.repeat(rowNumber);
}
```

## 66

- A function call allows you to actually use a function. You may not have been aware of it, but the methods like .push() that you have been using have been function calls.

A function is called by referencing the function's name, and adding (). Here's how to call a test function:

Example Code
test();
Replace the character.repeat(i + 1) in your .push() call with a function call for your padRow function.

```html
for (let i = 0; i < count; i = i + 1) {
  rows.push(padRow());
}
```

## 67

- Your padRow function has two parameters which you defined. Values are provided to those parameters when a function is called.

The values you provide to a function call are referred to as arguments, and you pass arguments to a function call. Here's a function call with "Hello" passed as an argument:

Example Code
test("Hello");
Pass i + 1 and count as the arguments to your padRow call. Like parameters, arguments are separated by a comma.

```html
for (let i = 0; i < count; i = i + 1) {
  rows.push(padRow(i + 1, count))
}
```

## 69

- Now it is time for a bit of math. Consider a three-row pyramid. If we want it centered, it would look something like:

Example Code
··#··
·###·
Empty spaces have been replaced with interpuncts, or middle dots, for readability. If you extrapolate the pattern, you can see that the spaces at the beginning and end of a row follow a pattern.

Update your blank space strings to be repeated rowCount - rowNumber times.

Open up the console to see the result.

```html
function padRow(rowNumber, rowCount) {
  return " ".repeat(rowCount - rowNumber) + character.repeat(rowNumber) + " ".repeat(rowCount - rowNumber);
}
```

## 70

- You can pass full expressions as an argument. The function will receive the result of evaluating that expression. For example, these two function calls would yield the same result:

Example Code
test(2 * 3 + 1);
test(7);
Looking at the pattern again:

Example Code
··#··
·###·
Update the character value to be repeated 2 * rowNumber - 1 times.

Open up the console again to see the updated result.

```html
function padRow(rowNumber, rowCount) {
  return " ".repeat(rowCount - rowNumber) + character.repeat(2 * rowNumber - 1) + " ".repeat(rowCount - rowNumber);
}
```

## 71

- Your pyramid generator now functions as expected. But this is an excellent opportunity to further explore the code you have written.

The addition operator is not the only way to add values to a variable. The addition assignment operator can be used as shorthand to mean "take the original value of the variable, add this value, and assign the result back to the variable." For example, these two statements would yield the same result:

Example Code
test = test + 1;
test += 1;
Update your iterator statement in the for loop to use addition assignment.

```html
for (let i = 0; i < count; i += 1)
```

## 72

- Because you are only increasing i by 1, you can use the increment operator ++. This operator increases the value of a variable by 1, updating the assignment for that variable. For example, test would become 8 here:

Example Code
let test = 7;
test++;
Replace your addition assignment with the increment operator for your loop iteration.

```html
for (let i = 0; i < count; i++)
```

## 73

- Rather than having to pass i + 1 to your padRow call, you could instead start your loop at 1. This would allow you to create a one-indexed loop.

Update your iterator to start at 1 instead of 0.

```html
for (let i = 1; i < count; i++) {
  rows.push(padRow(i + 1, count));
}
```

## 74

- The pyramid looks a little funny now. Because you are starting the loop at 1 instead of 0, you do not need to add one to i when you pass it to padRow.

Update the first argument of your padRow call to be i.

```html
for (let i = 1; i < count; i++) {
  rows.push(padRow(i, count));
}
```

## 75

- Unfortunately, now the bottom of the pyramid has disappeared. This is because you have created another off-by-one error.

Your original loop went for i values from 0 to 7, because count is 8 and your condition requires i to be less than count. Your loop is now running for i values from 1 to 7.

Your loop needs to be updated to run when i is 8, too. Looking at your logic, this means your loop should run when i is less than or equal to count. You can use the less than or equal to operator <= for this.

Update your loop condition to run while i is less than or equal to count.

```html
for (let i = 1; i <= count; i++) {
  rows.push(padRow(i, count));
}
```

## 76

- Comments can be helpful for explaining why your code takes a certain approach, or leaving to-do notes for your future self.

In JavaScript, you can use // to leave a single-line comment in your code.

Add a single-line comment above your function to remind yourself to change the code to a different kind of loop.

```html
//change code to different loop
for (let i = 1; i <= count; i++) {
  rows.push(padRow(i, count));
}
```

## 77

- JavaScript also has support for multi-line comments. A multi-line comment starts with

Unlike a single-line comment, a multi-line comment will encapsulate multiple lines.

 <!-- Use /* and */ to turn your current for loop, including the body, into a multi-line comment. -->

```html
/* for (let i = 1; i <= count; i++) {
  rows.push(padRow(i, count));
} */
```

## 78

- Your pyramid has disappeared again. That's okay - that is to be expected.

Before you create your new loop, you need to learn about if statements. An if statement allows you to run a block of code only when a condition is met. They use the following syntax:

Example Code
if (condition) {
  logic
}
Create an if statement with the boolean true as the condition. In the body, print the string "Condition is true".

```html
if (true) {
console.log("Condition is true")
}
```

## 79

- You'll see the string printed in the console, because true is in fact true.

Change the condition of your if statement to the boolean false.

```html
if (false) {
  console.log("Condition is true");
}
```

## 80

- Now the string is no longer printing, because false is not true. But what about other values?

Try changing the condition to the string "false".

```html
if ("false") {
  console.log("false");
}
```

## 81

- The text has appeared again! This is because "false" is a string, which when evaluated to a boolean becomes true. This means "false" is a truthy value.

A truthy value is a value that is considered true when evaluated as a boolean. Most of the values you encounter in JavaScript will be truthy.

A falsy value is the opposite - a value considered false when evaluated as a boolean. JavaScript has a defined list of falsy values. Some of them include false, 0, "", null, undefined, and NaN.

Try changing your if condition to an empty string "", which is a falsy value.

```html
if ("") {
  console.log("Condition is true");
}
```

## 82

- The text is gone again! Empty strings evaluate to false, making them a falsy value. You will learn more about truthy and falsy values in future projects.

In addition to if statements, JavaScript also has else if statements. else if statements allow you to check multiple conditions in a single block of code.

Here is the syntax for an else if statement:

Example Code
if (condition1) {
  // code to run if condition1 is true
} else if (condition2) {
  // code to run if condition2 is true
} else if (condition3) {
  // code to run if condition3 is true
}
If the first condition is false, JavaScript will check the next condition in the chain. If the second condition is false, JavaScript will check the third condition, and so on.

Below your if statement, add an else if statement that checks if 5 is less than 10. Then inside the body of the else if statement, log the string "5 is less than 10" to the console.

Check the console to see the results.

```html
if ("") {
  console.log("Condition is true");
}
else if (5 < 10) {
console.log("5 is less than 10");
}
```

## 83

- Sometimes you will want to run different code when all of the if...else if conditions are false. You can do this by adding an else block.

An else block will only evaluate if the conditions in the if and else if blocks are not met.

Here the else block is added to the else if block.

Example Code

if (condition) {
  // this code will run if condition is true
} else if (condition2) {
  // this code will run if the first condition is false
} else {
  // this code will run
  // if the first and second conditions are false
}
Add an else block to the else if block. Inside the else block, log the string "This is the else block" to the console.

To see the results in the console, you can manually change the < in the else if statement to >. That will make the condition false and the else block will run.

```html
if ("") {
  console.log("Condition is true");
} else if (5 > 10) {
  console.log("5 is less than 10");
} else {
  console.log("This is the else block");
}
```

## 84

- Now that you have practiced working with if...else if...else statements, you can remove them from your code.

Once you complete that, use let to declare a continueLoop variable and assign it the boolean false. Then use let to declare a done variable and assign it the value 0.

```html
let continueLoop = false;
let done = 0;
```

## 85

- A while loop will run over and over again until the condition specified is no longer true. It has the following syntax:

Example Code
while (condition) {
  logic;
}
Use that syntax to declare a while loop with continueLoop as the condition. The body should be empty.

```html
 let continueLoop = false;
let done = 0;
while (continueLoop) {

}
```

## 86

- Right now, if you change continueLoop to true, your while loop will run forever. This is called an infinite loop, and you should be careful to avoid these. An infinite loop can lock up your system, requiring a full restart to escape.

To avoid this, start by using the increment operator to increase the value of the done variable inside your loop.

```html
while (continueLoop) {
done++;
}
```

## 87

- The equality operator == is used to check if two values are equal. To compare two values, you'd use a statement like value == 8.

Below done++ inside your loop, add an if statement. The statement should check if done is equal to count using the equality operator.

```html
while (continueLoop) {
  done++;
  if (done == count) {

  }
}
```

## 88

- The equality operator can lead to some strange behavior in JavaScript. For example, "0" == 0 is true, even though one is a string and one is a number.

The strict equality operator === is used to check if two values are equal and share the same type. As a general rule, this is the equality operator you should always use. With the strict equality operator, "0" === 0 becomes false, because while they might have the same value of zero, they are not of the same type.

Update your done == count condition to use the strict equality operator.

```html
if (done === count) {

  }
```

## 89

- When done has reached the value of count, we want the loop to stop executing.

Inside your if body, assign the boolean false to your continueLoop variable.

```html
if (done === count) {
    continueLoop = false;
  }
 ```

## 90

- To make your pyramid generate again, push the result of calling padRow with done and count as the arguments to your rows array, similar to what you did in your first loop.

```html
rows.push(padRow(done, count));

 ```

## 91

- The strict inequality operator !== allows you to check if two values are not equal, or do not have the same type. The syntax is similar to the equality operator: value !== 4.

Update your while loop condition to check if done is not equal to count.

```html
while (done !== count) {
  done++;
  rows.push(padRow(done, count));
  if (done === count) {
    continueLoop = false;
  } 
}
 ```

## 92

- Since you have moved the comparison into the while condition, you can remove your entire if statement.

```html
while (done !== count) {
  done++;
  rows.push(padRow(done, count));
}
 ```

## 93

- Your loop is no longer relying on the continueLoop variable. This makes the variable an unused declaration. Generally, you want to avoid unused declarations to prevent future confusion.

Remove your continueLoop variable.

```html
let done = 0;

while (done !== count) {
  done++;
  rows.push(padRow(done, count));
}
 ```

## 94

- Your pyramid generator is still working. However, it could be possible to end up with an infinite loop again.

Because you are only checking if done is not equal to count, if done were to be larger than count your loop would go on forever.

Update your loop's condition to check if done is less than or equal to count.

```html
let done = 0;

while (done <= count) {
  done++;
  rows.push(padRow(done, count));
}
 ```

## 95

- Using done to track the number of rows that have been generated is functional, but you can actually clean up the logic a bit further.

Arrays have a special length property that allows you to see how many values, or elements, are in the array. You would access this property using syntax like myArray.length.

Note that rows.length in the padRow call would give you an off-by-one error, because done is incremented before the call.

Update your condition to check if rows.length is less than count.

```html
let done = 0;

while (rows.length < count) {
  done++;
  rows.push(padRow(done, count));
}
 ```

## 96

- Replace the done reference in your padRow call with rows.length + 1.

```html
let done = 0;

while (rows.length < count) {
  done++;
  rows.push(padRow(rows.length + 1, count));
}
 ```

## 97

- Now you no longer need your done variable. Remove the increment operation from your loop, and the variable declaration for done.

```html
while (rows.length < count) {
  rows.push(padRow(rows.length + 1, count));
}
```

## 98

- That's a very clean and functional loop. Nice work! But there's still more to explore.

Use a multi-line comment to comment out your while loop.

```html
That's a very clean and functional loop. Nice work! But there's still more to explore.

Use a multi-line comment to comment out your while loop.
```

## 99

- What if you made your pyramid upside-down, or inverted? Time to try it out!

Start by creating a new for loop. Declare your iterator i and assign it the value of count, then use the boolean false for your condition and iteration statements.

```html
for (let i = count; false; false) {

}
```

## 100

- Because you are going to loop in the opposite direction, your loop needs to run while i is greater than 0. You can use the greater than operator > for this.

Set your loop's condition to run when i is greater than 0.

```html
for (let i = count; i > 0; false) {

}
```

## 101

- Your iteration statement is also going to be different. Instead of adding 1 to i with each loop, you need to subtract 1.

Like you did earlier with i = i + 1, update your iteration statement to give i the value of subtracting 1 from itself.

```html
for (let i = count; i > 0; i = i - 1) {

}
```

## 102

- Again, push the result of calling padRow with your i and count variables to your rows array.

Open up the console to see the upside-down pyramid.

```html
for (let i = count; i > 0; i = i - 1) {
  rows.push(padRow(i, count));
}
```

## 103

- Just like addition, there are different operators you can use for subtraction. The subtraction assignment operator -= subtracts the given value from the current variable value, then assigns the result back to the variable.

Replace your iterator statement with the correct statement using the subtraction assignment operator.

```html
for (let i = count; i > 0; i -= 1) {
  rows.push(padRow(i, count));
}
```

## 104

- Because you are only subtracting one from i, you can use the decrement operator --.

Replace your subtraction assignment with the decrement operator.

```html
for (let i = count; i > 0; i--) {
  rows.push(padRow(i, count));
}
```

## 105

- Use a multi-line comment to comment out this loop as well, to prepare for the next approach.

```html
/* for (let i = count; i > 0; i--) {
  rows.push(padRow(i, count));
} */
```

## 106

- You can actually build the inverted pyramid without needing to loop "backwards" like you did.

To do this, you'll need to learn a couple of new array methods. Start by using const to declare a numbers variable. Assign it an array with the elements 1, 2, and 3. Then log the numbers array.

```html
const numbers = [1, 2, 3];
console.log(numbers);
```

## 107

- The .unshift() method of an array allows you to add a value to the beginning of the array, unlike .push() which adds the value at the end of the array. .unshift() returns the new length of the array it was called on.

Example Code
const countDown = [2, 1, 0];
const newLength = countDown.unshift(3);
console.log(countDown); // [3, 2, 1, 0]
console.log(newLength); // 4
Use const to declare an unshifted variable, and assign it the result of calling .unshift() on your numbers array. Pass 5 as the argument. Then print your unshifted variable.

```html
const numbers = [1, 2, 3];
const unshifted = numbers.unshift(5)
console.log(unshifted);
```

## 108

- Arrays also have a .shift() method. This will remove the first element of the array, unlike .pop() which removes the last element. Here is an example of the .shift() method:

Example Code
const numbers = [1, 2, 3];
numbers.shift();
The numbers array would be [2, 3].

Directly below your numbers array, declare a shifted variable and assign it the result of calling .shift() on the numbers array. On the next line, log the shifted variable to the console.

```html
const numbers = [1, 2, 3];
const shifted = numbers.shift();
console.log(shifted);
const unshifted = numbers.unshift(5);
console.log(unshifted);
console.log(numbers);
```

## 109

- Now that you've tried these methods, you can do another inverted pyramid approach. But first you need to clean up your experimentation.

Remove your numbers array, and the method calls and log calls.

```html
```

## 110

- Sometimes you may wish to bring back previous code that you commented out. You can do so by removing the around that code. This is called uncommenting.

Uncomment only your first for loop. Leave the single line comment and the other two multi line comments in place.

```html
// TODO: use a different type of loop
for (let i = 1; i <= count; i++) {
  rows.push(padRow(i, count));
}

/*while (rows.length < count) {
  rows.push(padRow(rows.length + 1, count));
}*/

/*for (let i = count; i > 0; i--) {
  rows.push(padRow(i, count));
}*/
```

## 111

- Your pyramid is no longer inverted. This is because you are adding new rows to the end of the array.

Update your loop body to add new rows to the beginning of the array.

```html
for (let i = 1; i <= count; i++) {
  rows.unshift(padRow(i, count));
}
```

## 112

- What if you had a way to toggle between an inverted pyramid and a standard pyramid?

Start by declaring an inverted variable, and assigning it the value true. You are not changing this variable in your code, but you will need to use let so our tests can modify it later.

```html
let inverted = true;
```

## 113

- Use an if statement to check if inverted is true. Remember that you do not need to use an equality operator here.

```html
for (let i = 1; i <= count; i++) {
  if (inverted) {

  }
  rows.unshift(padRow(i, count));
}
```

## 114

- Now move your .unshift() call into your if block.

```html
for (let i = 1; i <= count; i++) {
  if (inverted) {
    rows.unshift(padRow(i, count));
  }
}
```

## 115

- If your pyramid is not inverted, then you will want to have an else block that builds the pyramid in the normal order.

In earlier steps, you learned how to work with else statement like this:

Example Code
if (condition) {
  // if condition is true, run this code
} else {
  // if condition is false, run this code
}
Add an else block to your if block.

```html
for (let i = 1; i <= count; i++) {
  if (inverted) {
    rows.unshift(padRow(i, count));
  } else {
    
  }

}
```

## 116

- When inverted is false, you want to build a standard pyramid. Use .push() like you have in previous steps to achieve this.

```html
for (let i = 1; i <= count; i++) {
  if (inverted) {
    rows.unshift(padRow(i, count));
  } else {
    rows.push(padRow(i, count));
  }
}
```

## 117

- Your pyramid generator is now in a finished state, with more functionality than you originally planned! The next step is to clean up your code.

Remove all comments, both single- and multi-line, from your code.

```html

for (let i = 1; i <= count; i++) {
  if (inverted) {
    rows.unshift(padRow(i, count));
  } else {
    rows.push(padRow(i, count));
  }
}
```

## 118

- Nice work! Experiment with different values for your character, count, and inverted variables.

When you are ready to move on to your next project, set character to "!", count to 10, and inverted to false to continue.

Congratulations on completing your first JavaScript project!

```html
const character = "!";
const count = 10;
const rows = [];
let inverted = false;
```
