
## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
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

- View the optimal layout depending on their device's screen size
- See hover and focus states for interactive elements

### Screenshot

![](./images/Screenshot%20(343).png)

### Links

- Solution URL: [https://github.com/keerthana769/Product-preview-page-component/]
- Live Site URL: [https://keerthana769.github.io/Product-preview-page-component/]

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Mobile-first workflow

### What I learned

1. **Viewport height usage**

  - `height: 100vh` can be useful when content is smaller than the viewport
    It should be avoided when content may exceed the viewport, as it can cause compression issues
  - `align-items: center` works best when content height is less than the viewport height

2. **Border-radius and images**

  - Images do not automatically respect a parent container’s `border-radius`
  - By default, images can overflow their parent and hide rounded corners
  - The solution is to clip the content using `overflow: hidden` on the container

  ```css
  .container {
    border-radius: 16px;
    overflow: hidden;
  }
  ```

3. **Responsive images with <picture>**

  - When different image files are provided for mobile and desktop, the `<picture>` element is the correct approach
  - Larger screen sources must come first. The `<img>` element should be last as a fallback
  - `<source>` only works inside `<picture>` (or `<audio>`/`<video>`)
  ```html
  <picture>
    <source srcset="./assets/image-desktop.jpg" media="(min-width: 768px)">
    <img src="./assets/image-mobile.jpg" alt="Product image">
  </picture>
  ```

4. **Avoid fixed heights**

    Using fixed or max heights on content-based layouts can cause:
    - Text overflow
    - Clipped buttons
    - Layout issues when zooming or using accessibility settings

    A better approach is to: Control width, let height be content-driven.

### Continued development

I would like to explore writing styles using a CSS preprocessor such as Sass.
At the moment, I chose to focus on strengthening my core CSS fundamentals before introducing additional tools.

### Useful resources

- [Resource 1](https://sass-lang.com/guide/) - Helpful introduction to Sass( CSS preprocessors).

## Author

- Frontend Mentor - [@keerthana769](https://www.frontendmentor.io/profile/keerthana769)
- LinkedIn - [@keerthana-gurram](https://www.linkedin.com/in/keerthana-gurram/)



