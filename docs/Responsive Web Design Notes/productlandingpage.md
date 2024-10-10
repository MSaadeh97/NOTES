# landing page

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta name="description" content="freeCodeCamp Accessibility Quiz practice project" />
    <title>Accessibility Quiz</title>
    <link rel="stylesheet" href="styles.css" />
  </head>
  <body>
    <header id="header">
      <img src="https://cdn.freecodecamp.org/testable-projects-fcc/images/product-landing-page-logo.png" alt="trombone" id="header-img" class="img1" />
      <nav id="nav-bar">
        <ul>
          <li><a href="#features" class="nav-link">Features</a></li>
          <li><a href="#How-It-Works" class="nav-link">How It Works</a></li>
          <li><a href="#Pricing" class="nav-link">Pricing</a></li>
        </ul>
        </nav>
    </header>
    <main>
        <section class="sec1">
          <h2>Handcrafted, home-made masterpieces</h2>
          <form method="post" action="https://www.freecodecamp.com/email-submit" id="form">
          <div class="emailer">
            <label for="email"></label>
            <input type="email" name="email" id="email" placeholder="Enter your email address" required />
          </div>
          <input id="submit" type="submit" value="get started" class="btn" />
          </form>
        </section>
        <div class="container">
        <section id="features">
          <div class="grid">
            <div class="icon">
              <i class="fa fa=3x fa-fire">
                </i>
                </div>
                </div>
          <div class="desc">
            <h2>Premium Materials</h2>
              <p>Our trombones use the shiniest brass which is sourced locally. This will increase the longevity of your purchase.</p>
            </div>
            <div class="desc">
            <h2>Fast Shipping</h2>
              <p>We make sure you recieve your trombone as soon as we have finished making it. We also provide free returns if you are not satisfied.</p>
            </div>
            <div class="desc">
            <h2>Quality Assurance</h2>
              <p>For every purchase you make, we will ensure there are no damages or faults and we will check and test the pitch of your instrument.</p>
            </div>
          </section>
        </div>
        <section id="How-It-Works">
<iframe width="560" height="315" src="https://www.youtube.com/embed/y8Yv4pnO7qc" title="Roman Carnival Overture Op. 9 for Five Trombones" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" id="video" allowfullscreen></iframe>
          </section>
          <section id="Pricing">
            <div class="product" id="tenor">
              <div class="level">Tenor Trombone</div>
              <h2>$600</h2>
              <ol>
                <li>Lorem ipsum.</li>
                <li>Lorem ipsum.</li>
                <li>Lorem ipsum donor.</li>
                <li>Lorem ipsum.</li>
                </ol>
                <button class="btn">Select</button>
              </div>
              <div class="product" id="bass">
              <div class="level">Bass Trombone</div>
              <h2>$900</h2>
              <ol>
                <li>Lorem ipsum.</li>
                <li>Lorem ipsum.</li>
                <li>Lorem ipsum dolor.</li>
                <li>Lorem ipsum.</li>
                </ol>
                <button class="btn">Select</button>
              </div>
              <div class="product" id="bass">
              <div class="level">Valve Trombone</div>
              <h2>$1200</h2>
              <ol>
                <li>Plays similar to a Trumpet</li>
                <li>Great for Jazz Bands</li>
                <li>Lorem ipsum dolor.</li>
                <li>Lorem ipsum.</li>
                </ol>
                <button class="btn">Select</button>
              </div>
            </section>
    </main>
    <footer>
      <nav>
        <ul>
          <li><a href="#">Privacy</a></li>
          <li><a href="#">Terms</a></li>
          <li><a href="#">Contact</a></li>
        </ul>
        <span>Copyright 2016, Orignal Trombones</span>
        </nav>
    </footer>
  </body>
</html>

CSS 

footer  span {
      margin-top: 5px;
    display: flex;
    justify-content: flex-end;
    font-size: 0.9em;
    color: #444;
}
.product {
      display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
    width: calc(100% / 3);
    margin: 10px;
    border: 1px solid #000;
    border-radius: 3px;
}
iframe {
      overflow-clip-margin: content-box !important;
    overflow: clip !important;
    border-width: 2px;
    border-style: inset;
    border-color: initial;
    border-image: initial;
}

#How-It-Works {
      margin-top: 50px;
    display: flex;
    justify-content: center;
}

html {
      display: block;
}

@media (prefers-reduced-motion: no-preference) {
  * {
    scroll-behavior: smooth;
  }
}

img {
  width: 45%;
  object-fit: cover;
}

nav {
  font-weight: 400;
}

nav > ul {
      width: 35vw;
    display: flex;
    flex-direction: row;
    justify-content: space-around;
}

* {
      margin: 0;
    padding: 0;
    box-sizing: border-box;
}

ul {
      display: block;
    list-style-type: disc;
    margin-block-start: 1em;
    margin-block-end: 1em;
    margin-inline-start: 0px;
    margin-inline-end: 0px;
    padding-inline-start: 40px;
    unicode-bidi: isolate;
}

body {
  background-color: #eee;
}

a {
      color: #000;
    text-decoration: none;
}

li {
      list-style: none;
}

.sec1 {
      display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    text-align: center;
    height: 200px;
    margin-top: 50px;
}

h2 {
      display: block;
    font-size: 1.5em;
    margin-block-start: 0.83em;
    margin-block-end: 0.83em;
    margin-inline-start: 0px;
    margin-inline-end: 0px;
    font-weight: bold;
    unicode-bidi: isolate;
}

#sec1 > h2 {
      margin-bottom: 20px;
    word-wrap: break-word;
}

form {
      display: block;
    margin-top: 0em;
    unicode-bidi: isolate;
}

p {
      display: block;
    margin-block-start: 1em;
    margin-block-end: 1em;
    margin-inline-start: 0px;
    margin-inline-end: 0px;
    unicode-bidi: isolate;
}

#features .desc {
      display: flex;
    flex-direction: column;
    justify-content: center;
    height: 125px;
    width: 80vw;
    padding: 5px;
}

div {
      display: block;
    unicode-bidi: isolate;
}
.container {
      max-width: 1000px;
    width: 100%;
    margin: 0 auto;
}

.grid {
    display: flex;
}

.product > button {
      border: 0;
    margin: 15px 0;
    background-color: #f1c40f;
    font-weight: 400;
}

.btn {
      padding: 0 20px;
    height: 40px;
    font-size: 1em;
    font-weight: 900;
    text-transform: uppercase;
    border: 3px black solid;
    border-radius: 2px;
    background: transparent;
    cursor: pointer;
}

button {
      appearance: auto;
    text-rendering: auto;
    color: buttontext;
    letter-spacing: normal;
    word-spacing: normal;
    line-height: normal;
    text-transform: none;
    text-indent: 0px;
    text-shadow: none;
    display: inline-block;
    text-align: center;
    align-items: flex-start;
    cursor: default;
    box-sizing: border-box;
    background-color: buttonface;
    margin: 0em;
    padding-block: 1px;
    padding-inline: 6px;
    border-width: 2px;
    border-style: outset;
    border-color: buttonborder;
    border-image: initial;
}
```
