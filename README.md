# ArthurGC Portfolio

This is the first version of my portfolio, it still needs more complexity.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the site depending on their device's screen size
- See hover states for all interactive elements on the page

### Links

- Live Site URL: [Preview Live Here](https://arthurgc.github.io/portfolio/)

## My process

### Built with

- Semantic HTML5 markup
- CSS and SASS custom properties
- Flexbox
- Mobile-first workflow
- Media Query

### What I learned

I had some issues with `navbar__menu > a:hover` because for media queries I couldn't remove it, even I use all: unset. That's why I had to add hover effects in media queries instead of in the mobile view css.

```css
/* Cause issues in other media queries */
.navbar{
    &__menu{
        a{
          &:hover{
                    color: #000;
                    background: $clr-primary-very-light-blue;
                }
        }
    }
}
```
```css
/* The solution */
@media (max-width: 767px) {
    .navbar{
        &__menu{
            a{
                &:hover{
                    color: #000;
                    background: $clr-primary-very-light-blue;
                }
            }
        }
    }
    
}
```

## Author

- Github - [ArthurGC](https://github.com/ArthurGC)
