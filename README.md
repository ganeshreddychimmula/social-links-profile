# Frontend Mentor - Social links profile solution

This is a solution to the [Social links profile challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/social-links-profile-UG32l9m6dQ). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Useful resources](#useful-resources)
- [Author](#author)
- [Acknowledgments](#acknowledgments)


## Overview

### The challenge

Users should be able to:

- See hover and focus states for all interactive elements on the page

### Screenshot

[Visit the site here]()
![Scrrenshot](./design/images/image.png)


### Links

- Solution URL: [Github](https://github.com/ganeshreddychimmula/social-links-profile)
- Live Site URL: [Live site](https://ganeshreddychimmula.github.io/social-links-profile/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow

### What I learned

Recap over some of your major learnings while working through this project.
To see how you can add code snippets, see below:

If you want more help with writing markdown, we'd recommend checking out [The Markdown Guide](https://www.markdownguide.org/) to learn more.

**How to pick Correct Semantical Elements?**
__Semantic HTML Structure__

Used semantic elements like `<figure>` for the avatar, `<section>` for name/location, and `<nav>` for social links.
- **Add `alt` to `<img>`**  
  Improves accessibility for screen readers.
- **Wrap everything in an `<article>`**  
  The profile card is a self-contained piece of content.
- **Use `<header>` instead of `<section>`**  
  Ideal for grouping name and location as introductory content.\
- **Replace `<button>`s in `<nav>` with `<ul>` and `<a>` links**  
  Navigation is a list of links, not actions — helps with semantics and screen reader navigation.
- **Maintain proper heading levels**  
  Avoid skipping levels like `<h2>` → `<h4>` without nesting.

These changes enhance the **semantic clarity**, **accessibility**, and **maintainability** of the HTML structure.

**Custom fonts**
When you have multiple variations of the same font family with different weights and styles, you should use multiple @font-face declarations with the same font-family name but different font-weight and font-style properties. Here's how to properly set this up:
```css
@font-face {
  font-family: 'my-custom-font';
  src: url('path/to/variable-font.woff2') format('woff2-variations');
  font-weight: 100 900; /* Specify the weight range supported by the variable font */
  font-style: normal;
  font-display: swap; /* Optional but recommended for performance */
}

/* Regular/Normal weight */
@font-face {
  font-family: 'my-custom-font';
  src: url('path/to/font-regular.woff2') format('woff2');
  font-weight: 400; /* or 'normal' */
  font-style: normal;
}

/* Bold weight */
@font-face {
  font-family: 'my-custom-font';
  src: url('path/to/font-bold.woff2') format('woff2');
  font-weight: 700; /* or 'bold' */
  font-style: normal;
}

/* Italic style */
@font-face {
  font-family: 'my-custom-font';
  src: url('path/to/font-italic.woff2') format('woff2');
  font-weight: 400;
  font-style: italic;
}
```
For different font sizes, you don't need separate @font-face declarations, as font size is controlled separately using the font-size property:
```css
h1 {
  font-family: 'my-custom-font', Arial, sans-serif;
  font-weight: 700;
  font-size: 2.5rem; /* Large size */
}

p {
  font-family: 'my-custom-font', Arial, sans-serif;
  font-weight: 400;
  font-size: 1rem; /* Medium size */
}

.small-text {
  font-family: 'my-custom-font', Arial, sans-serif;
  font-weight: 400;
  font-size: 0.8rem; /* Small size */
}
```
**Fall back Fonts**

This is an excellent fallback stack for your Inter Variable font. Let me break down why this is a good choice:

```css
font-family: 'my-font', /* Your Inter Variable font */
             system-ui, 
             -apple-system, BlinkMacSystemFont,
             'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 
             'Open Sans', 'Helvetica Neue', 
             sans-serif;
```

This stack provides comprehensive coverage:

1. **system-ui**: Modern approach that automatically selects the native UI font of the user's operating system

2. **-apple-system, BlinkMacSystemFont**: Target San Francisco on Apple devices

3. **Segoe UI**: Windows default UI font

4. **Roboto**: Android's system font 

5. **Oxygen, Ubuntu, Cantarell**: Common Linux distribution fonts

6. **Open Sans**: Very popular web font with good readability similar to Inter

7. **Helvetica Neue**: Classic choice for Apple users on older systems

8. **sans-serif**: Final generic fallback

This stack is particularly well-suited for Inter because it prioritizes modern UI system fonts that share Inter's characteristics: good readability, neutral design, and optimization for screen display. The progression moves from most similar to Inter toward more universally available options.

This is a robust, comprehensive approach that will maintain a consistent user experience across virtually all devices and platforms.

**Don't forget to Use flew grow,shrink, basis**

**Remove bullet points of list**
liststyle:none


### Useful resources

- [Semantic structure](https://www.example.com)
- [Git sheet](https://cs.fyi/guide/git-cheatsheet)


## Author

- Frontend Mentor - [@ganeshreddychimmula](https://www.frontendmentor.io/profile/@ganeshreddychimmula)

