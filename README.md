# Frontend Mentor - Product preview card component solution

This is a solution to the [Product preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/product-preview-card-component-GO7UmttRfa). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Frontend Mentor - Product preview card component solution](#frontend-mentor---product-preview-card-component-solution)
  - [Table of contents](#table-of-contents)
  - [Overview](#overview)
    - [The challenge](#the-challenge)
    - [Screenshot](#screenshot)
    - [Links](#links)
  - [My process](#my-process)
    - [Built with](#built-with)
    - [What I learned](#what-i-learned)
    - [Useful resources](#useful-resources)
  - [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover and focus states for interactive elements

### Screenshot

![Screenshot](./screenshot.jpg)

### Links

- [Solution URL]()
- [Live Site URL]()

## My process

### Built with

- Plain HTML
- [Tailwind CSS](https://tailwindcss.com/)

### What I learned

In this challenge,I learned how to apply Tailwind CSS into a plain HTML project. First, initiate `package.json`

```bash
yarn init -y
```

Install `tailwindcss`, `postcss-cli`, and `autoprefixer`

```bash
yarn add tailwindcss  -D
```

Create `tailwind.config.js`

```bash
npx tailwindcss init
```

create `index.html` and add the path into `content` in `tailwind.config.js`

```javascript
/* tailwind.config.js */
module.exports = {
  content: [
    './*.html',
  ],
  /* ... */
}
```

Create `tailwind.css` and add Tailwind directives

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

Create a script called `watch` on `package.json`

```json
{
  "scripts": {
    "watch": "tailwindcss -i ./tailwind.css -o ./style.css --watch"
  },
}
```

Run `watch` script. This will create a new CSS file named `style.css`

```bash
yarn watch
```

Import `style.css` to `index.html`

```html
<!doctype html>
<html>
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link rel="stylesheet" href="style.css" />
</head>
<body>
</body>
</html>
```

To serve the page, install [live-server](https://www.npmjs.com/package/live-server) globally and run this command:

```bash
live-server --host=localhost
```

Everytime you utilize any class from the Tailwind library while running `watch`, tailwind updates `style.css` to make sure only used classes written upon built.

### Useful resources

- [Automatic Class Sorting with Prettier](https://tailwindcss.com/blog/automatic-class-sorting-with-prettier) - This helped me sorting Tailwind classes.

## Author

- Website - [vyonizr](https://vyonizr.com/)
- Frontend Mentor - [@vyonizr](https://www.frontendmentor.io/profile/vyonizr)
