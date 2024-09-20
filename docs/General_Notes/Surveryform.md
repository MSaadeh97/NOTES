# Building a Survery form

```html

<!DOCTYPE html>
<html lang="en">
<head>
  <title> Survey Form </title>
  <meta charset="UTF-8" />
  <link rel="stylesheet" href="styles.css" />
</head>
<body>
  <h1 id="title">Survey Form</h1>
  <p id="description"> Description</p>
  <form method="post" action="https://register-demo.freecodecamp.org" id="survey-form">
  <fieldset>
        <label for="name-label">Name <input id="name-label" name="name-label" type="text" placeholder="Enter your name" required /></label>
        <label for="email-label">Email <input id="email-label" name="email-label" type="email" placeholder="Enter your email" required /></label>
        <label for="number-label">Age (optional) <input id="number-label" type="number" name="number-label" min="10" max="99" placeholder="Age" /></label>
        <label for="dropdown"> Which option best describes your current role?
          <select id="dropdown" name="dropdown">
            <option value="">(Select current role)</option>
            <option value="1">Student</option>
            <option value="2">Full Time Job</option>
            <option value="3">Full Time Learner</option>
            <option value="5">Prefer not to say</option>
            <option value="5">Other</option>
          </select>
        </label>
  </fieldset>
  <fieldset>
        <legend>Would you recommend freeCodeCamp to a friend?</legend>
        <label for="definitely"><input id="definitely" type="radio" name="choice" class="inline" checked /> Definitely</label>
        <label for="maybe"><input id="maybe" type="radio" name="choice" class="inline" /> Maybe</label>
        <label for="notsure"><input id="notsure" type="radio" name="choice" class="inline" checked /> Not sure</label>
      </fieldset>
<fieldset>
  <label for="option"> What is your favorite feature of freeCodeCamp?
          <select id="option" name="option">
            <option value="">(Select an option)</option>
            <option value="1">Challenges</option>
            <option value="2">Projects</option>
            <option value="3">Community</option>
            <option value="5">Open Source</option>
          </select>
        </label>
</fieldset>
<fieldset>
  <legend>What would you like to see improved? (Check all that apply)</legend>
 <input id="Front-end Projects" type="checkbox" name="choices" value="Front-end Projects" class="inline" checked><label for="Front-end Projects" class="inline">Front-end Projects</label>
  <input id="Back-end Projects" type="checkbox" name="choices" value="Back-end Projects"> <label for="Back-end Projects">Back-end Projects</label>
  <input id="Data Visualization" type="checkbox" name="choices" value="Data Visualization"> <label for="Data Visualization">Data Visualization</label>
  <input id="Challenges" type="checkbox" name="choices" value="Challenges"> <label for="Challenges">Challenges</label>
  <input id="Open Source Community" type="checkbox" name="choices" value="Open Source Community"> <label for="Open Source Community">Open Source Community</label>
  <input id="Gitter help rooms" type="checkbox" name="choices" value="Gitter help rooms"> <label for="Gitter help rooms">Gitter help rooms</label>
  <input id="Videos" type="checkbox" name="choices" value="Videos"> <label for="Videos">Videos</label>
  <input id="City Meetups" type="checkbox" name="choices" value="City Meetups"> <label for="City Meetups">City Meetups</label>
  <input id="Wiki" type="checkbox" name="choices" value="Wiki"> <label for="Wiki">Wiki</label>
  <input id="Forum" type="checkbox" name="choices" value="Forum"> <label for="Forum">Forum</label>
  <input id="Additional Courses" type="checkbox" name="choices" value="Additional Courses"> <label for="Additional Courses">Additional Courses</label>
</fieldset>
<fieldset>
<label for="bio">Any comments or suggestions?
  <textarea id="bio" name="bio" rows="4" cols="30"    placeholder="Enter your comment here..."></textarea>
</label>
<input type="submit" value="Submit" />
</fieldset>
</form>

</body>
</html>

```

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
  padding-bottom: 2em;
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

input[type="submit"] {
  display: block;
  width: 60%;
  margin: 1em auto;
  height: 2em;
  font-size: 1.1rem;
  background-color: #3b3b4f;
  border-color: white;
  min-width: 300px;
}

input[type="file"] {
  padding: 1px 2px;
}

.inline{
  display: inline; 
}

```
