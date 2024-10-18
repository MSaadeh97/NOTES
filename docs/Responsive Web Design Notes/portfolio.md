# portfolio

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta name="description" content="freeCodeCamp Accessibility Quiz practice project" />
    <title>Portfolio</title>
    <link rel="stylesheet" href="styles.css" />
  </head>
  <body>
    <header id="header">
      <nav id="navbar" class="nav">
        <ul class="nav-list">
          <li><a href="#welcome-section">About</a></li>
          <li><a href="#projects">Work</a></li>
          <li><a href="#contact">Contact</a></li>
        </ul>
        </nav>
    </header>
<main>
  <section id="welcome-section" class="welcome">
    <h1>Hey I am Mohammad</h1>
    <p>a web developer</p>
  </section>
  <section class="projects-section" id="projects">
      <h2 class="project-section-header"> These are some of my projects</h2>
      <div class="projects-grid">
<a href="https://codepen.io/freeCodeCamp/full/zNqgVx" target="_blank" class="project project-tile">
          <img class="project-image" src="https://cdn.freecodecamp.org/testable-projects-fcc/images/tribute.jpg" alt="project">
          <p class="project-title">
            <span class="code">&lt;</span>
            Tribute Page
            <span class="code">/&gt;</span>
          </p>
        </a>
        </div>
  </section>
  <section class="contact-section" id="contact">
    <div class="contact-section-header">
      <h2> Let's work together...</h2>
      <p> How do you take your coffee?</p>
    </div>
    <div class="contact-links">
      <a href="https://facebook.com/freecodecamp" target="_blank" class="btn contact-details" id="profile-link"><i class="fab fa-facebook-square"></i> Facebook</a>
      </div>
  </section>
  <footer>
    <p>My Portfolio @2024</p>
    <p>© Created for <a href="https://www.freecodecamp.com/" target="_blank">freeCodeCamp <i class="fab fa-free-code-camp"></i></a> </p>
  </footer>
</main>
</body>
</html>

CSS

.nav {
      display: flex;
    justify-content: flex-end;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    background: var(--main-red);
    box-shadow: 0 2px 0 rgba(0, 0, 0, 0.4);
    z-index: 10;
}

* {
      margin: 0;
    padding: 0;
}

nav {
      display: block;
    unicode-bidi: isolate;
}

body {
      font-family: 'Poppins', sans-serif;
    font-size: 1.8rem;
    font-weight: 400;
    line-height: 1.4;
    color: var(--main-white);
}

:root {
      --main-white: #f0f0f0;
    --main-red: #be3144;
    --main-blue: #45567d;
    --main-gray: #303841;
}

@media (max-width: 61.25em) {
  html {
    font-size: 58%;
}
}

@media (max-width: 61.25em) {
  html {
    font-size: 60%;
}
}

html {
    font-size: 62.5%;
}

*, *::before, *::after {
      box-sizing: inherit;
}

.nav-list {
      display: flex;
    margin-right: 2rem;
}

ul {
      list-style: none;
    margin-block-start: 1em;
    margin-block-end: 1em;
    margin-inline-start: 0px;
    margin-inline-end: 0px;
    padding-inline-start: 40px;
    unicode-bidi: isolate;
}



.welcome-section {
      display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 100%;
    height: 100vh;
    background-color: #000;
    background-image: linear-gradient(62deg, #3a3d40 0%, #181719 100%);
}

section {
  unicode-bidi: isolate;
}

.projects-section {
      text-align: center;
    padding: 10rem 2rem;
    background: var(--main-blue);
}

.projects-section-header {
      max-width: 640px;
    margin: 0 auto 6rem auto;
    border-bottom: 0.2rem solid var(--main-white);
}

h2 {
      font-size: 4.2rem;
          display: block;
    margin-block-start: 0.83em;
    margin-block-end: 0.83em;
    margin-inline-start: 0px;
    margin-inline-end: 0px;
    font-weight: bold;
    unicode-bidi: isolate;
}

h1, h2 {
      font-family: 'Raleway', sans-serif;
    font-weight: 700;
    text-align: center;
}

.projects-grid {
      display: grid;
    grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
    grid-gap: 4rem;
    width: 100%;
    max-width: 1280px;
    margin: 0 auto;
    margin-bottom: 6rem;
}

div {
    unicode-bidi: isolate;
}

a {
      text-decoration: none;
    color: var(--main-white);
}

a:-webkit-any-link {
  cursor: pointer;
}

.project {
      background: var(--main-gray);
    box-shadow: 1px 1px 2px rgba(0, 0, 0, 0.5);
    border-radius: 2px;
}

.project-image {
      height: calc(100% - 6.8rem);
    width: 100%;
    object-fit: cover;
}

img {
  display: block;
      overflow-clip-margin: content-box;
    overflow: clip;
}

.project-title {
      font-size: 2rem;
    padding: 2rem 0.5rem;
}

.code {
      color: var(--main-gray);
    transition: color 0.3s ease-out;
}

.contact-section {
      display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    width: 100%;
    height: 80vh;
    padding: 0 2rem;
    background: var(--main-gray);
}

.contact-links {
      display: flex;
    justify-content: center;
    width: 100%;
    max-width: 980px;
    margin-top: 4rem;
    flex-wrap: wrap;
}

.contact-details {
      font-size: 2.4rem;
    text-shadow: 2px 2px 1px #1f1f1f;
    transition: transform 0.3s ease-out;
}

.btn {
      display: inline-block;
    padding: 1rem 2rem;
    border-radius: 2px;
}

.fa, .fab, .fal, .far, .fas {
      -moz-osx-font-smoothing: grayscale;
    -webkit-font-smoothing: antialiased;
    display: inline-block;
    font-style: normal;
    font-variant: normal;
    text-rendering: auto;
    line-height: 1;
}

footer i {
      vertical-align: middle;
}

footer {
      font-weight: 300;
    display: flex;
    justify-content: space-evenly;
    padding: 2rem;
    background: var(--main-gray);
    border-top: 4px solid var(--main-red);
}
```
