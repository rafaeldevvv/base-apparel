# Frontend Mentor - Base Apparel coming soon page solution

This is a solution to the [Base Apparel coming soon page challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/base-apparel-coming-soon-page-5d46b47f8db8a7063f9331a0). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the site depending on their device's screen size
- See hover states for all interactive elements on the page
- Receive an error message when the `form` is submitted if:
  - The `input` field is empty
  - The email address is not formatted correctly

### Links

- Solution URL: [here](https://github.com/rafaeldevvv/base-apparel)
- Live Site URL: [here](https://rafaeldevvv.github.io/base-apparel/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow
- SASS
- JavaScript

### What I learned

I knew about this before but it was the first time I used it and it was quite useful. I was thinking of using background image with css, but this is simpler and easier.
```html
<picture id="hero">
  <source
    media="(min-width: 576px)"
    srcset="./images/hero-desktop.jpg"
    class="hero-img"
  />
  <img src="./images/hero-mobile.jpg" alt="Beautiful woman" class="hero-img" />
</picture>
```

This was a challenge at first but after some thought I figured out a way to position these.
```scss
.form-field {
  position: relative;

  input,
  button {
    border: 0;
    outline: 0;
    display: block;
    border-radius: 30px;
    padding: 1.4em 2.5em;
  }

  input {
    border: 1px solid $desaturated-red;
    width: 100%;
    padding-right: 34%;
  }
  input::placeholder {
    color: $desaturated-red;
  }

  button {
    position: absolute;
    z-index: 1;
    inset: 0 0 0 auto;
    margin: -1px 0;
    width: 22.5%;

    cursor: pointer;
    box-shadow: 0 15px 35px rgba(255, 0, 0, 0.2);
    background: url("../images/icon-arrow.svg") center center no-repeat, $second-gradient;
  }

  button:hover {
    background: url("../images/icon-arrow.svg") center center no-repeat, $first-gradient;
  }

  .failure-icon {
    position: absolute;
    right: calc(22.5% + 10px);
    top: 50%;
    transform: translateY(-50%);
    display: none;
  }
}
```

classList is awesome.

```js
if (!emailExp.test(email)) {
  field.classList.add("failure");
  outMessage.textContent = "Please provide a valid email";
} else {
  field.classList.remove("failure");
  outMessage.textContent = "👍";
}
```

### Continued development

I want to reinforce my knowledge on responsive web design.

### Useful resources

- [mozilla](https://developer.mozilla.org/en-US/docs/Web/API/Element/classList) - I quickly learned about classList here.
- [debuggex](https://www.debuggex.com/) - This is an amazing site to understand regular expressions.

## Author

- Frontend Mentor - [@rafaeldevvv](https://www.frontendmentor.io/profile/rafaeldevvv)
- Instagram - [@rafffael_maia](https://www.instagram.com/rafffael_maia)
