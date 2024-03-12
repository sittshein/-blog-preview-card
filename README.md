# Frontend Mentor - Blog preview card solution

This is a solution to the [Blog preview card challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/blog-preview-card-ckPaj01IcS). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Frontend Mentor - Blog preview card solution](#frontend-mentor---blog-preview-card-solution)
  - [Table of contents](#table-of-contents)
  - [Overview](#overview)
    - [The challenge](#the-challenge)
    - [Screenshot](#screenshot)
    - [Links](#links)
  - [My process](#my-process)
    - [Built with](#built-with)
    - [What I learned](#what-i-learned)
    - [Continued development](#continued-development)
    - [Useful resources](#useful-resources)

## Overview

### The challenge

Users should be able to:

- See hover and focus states for all interactive elements on the page

### Screenshot

![](./screenshot.jpg)

Add a screenshot of your solution. The easiest way to do this is to use Firefox to view your project, right-click the page and select "Take a Screenshot". You can choose either a full-height screenshot or a cropped one based on how long the page is. If it's very long, it might be best to crop it.

Alternatively, you can use a tool like [FireShot](https://getfireshot.com/) to take the screenshot. FireShot has a free option, so you don't need to purchase it. 

Then crop/optimize/edit your image however you like, add it to your project, and update the file path in the image above.

**Note: Delete this note and the paragraphs above when you add your screenshot. If you prefer not to add a screenshot, feel free to remove this entire section.**

### Links

- Solution URL: [Go to solution URL](https://github.com/sittshein/blog-preview-card-challenge)
- Live Site URL: [Go to live site](https://blog-preview-card-challenge-nine.vercel.app/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Mobile-first workflow
- [Less](https://lesscss.org/) - Less.js for style css

### What I learned

- I have learnt when to apply `background` property instead of `img` tag.
- I have learnt how to use CSS's transition and transform property. 

To see how you can add code snippets, see below:

```html
<div class="blog-post">
  <div class="image"></div>
</div>
```
```css
.blog-post {
  .image {
    height: 200px;
    border-radius: 10px;
    background: url("./assets/images/illustration-article.svg") center/cover no-repeat border-box;
  }
}
```
```html
<div class="card has-transition">
  ....
</div>
```
```css
@media only screen and (min-width: @breakpoints[desktop]) {
  .card {
    .rounded-box(@width:384px);

    &.has-transition {
      transition-property: box-shadow, transform, width;
      transition-duration: 300ms;
      transition-timing-function: ease;
    }

    &:is(:hover, :focus) {
      box-shadow: 16px 16px 0 0 rgba(0, 0, 0, 0.75);
      transform: translateY(-8px);
    }

    & .blog-post .content .category a {
      .typography(14px, @weight[bold]);
    }

    & .blog-post .content .title a {
      .typography(24px, @weight[bold]);

      &:is(:hover, :focus) {
        color: @colors[yellow];
      }
    }

    & .blog-post .content .description {
      .typography(16px, @weight[regular], @colors[grey]);
    }
  }
}
```


### Continued development


### Useful resources

- [web.dev | css backgrounds](https://web.dev/learn/css/backgrounds) - This is an amazing article which helped me finally understand CSS background prperties. I'd recommend it to anyone still learning this concept.
- [web.dev | css transitions](https://web.dev/learn/css/transitions) - This is an amazing article which helped me finally understand CSS transitions. I'd recommend it to anyone still learning this concept.
