# Frontend Mentor - NFT preview card component solution

This is a solution to the [NFT preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/nft-preview-card-component-SbdUL_w0U). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size:
    - Mobile layout viewed at max-width 1439px
    - Desktop layout viewed at min-width 1440px
- See hover states for interactive elements:
    - NFT image with semi-transparent overlay with eye svg
    - Font color change for name of NFT
    - Font color change for name of NFT creator

### Screenshot

![Mobile](https://i.imgur.com/AnGRUSD.png)
![Desktop](https://i.imgur.com/u2GRLXY.png)
![Desktop - View image hover state](https://i.imgur.com/pAV4OoY.png)
![Desktop - NFT name hover state](https://i.imgur.com/WGfdjJv.png)
![Desktop - Creator name hover state](https://i.imgur.com/L0AiNm5.png)

### Links

- [GitHub Repo](https://github.com/rjcrowderschaefer/fm-nft-preview-card-component)
- [Live Site URL](https://main--stalwart-halva-9131b6.netlify.app/)

## My process

I used a mobile first approach to develop this process, beginning with the mobile layout and expanding to the desktop layout using a CSS media query. Where possible I used semantic HTML and was diligent on when and where I used classes versus ids throughout the development process.

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Mobile-first workflow

### What I learned

This was a straightforward project and great practice at using Flexbox to align elements as desired. Additionally, I learned that :hover can be applied to elements beyond `a` tags/links and expanded my use of the ::before attribute in my CSS to adjust the width, height, opacity, color and other properties of the layer overlay on the NFT image to align with the design specs. This was a fun project that demonstrated how my frontend dev skills have developd over the past 8 months.

A code snippet that I'm proud of:

```css
.overlay {
    position: relative;
    display: inline-block;
}

.overlay > img {
    vertical-align: middle;
}

.overlay::before {
    content: "";
    position: absolute;
    left: 24.5px;
    top: 24.5px;
    width: 278px;
    height: 278px;
    border-radius: 10px;
    background: cyan;
    opacity: 0;
    transition: .5s ease;
    cursor: pointer;
}

.view {
    display: none;
    position: absolute;
    top: 50%;
    left: 139px;
    cursor: pointer;
    z-index: 1
}

.overlay:hover::before {
    opacity: 0.5;
}

.overlay:hover .view {
    display: inline;
}
```
<!-- Troubleshooting the best way to include the semi-transparent hover state on the NFT image was interesting. The code above is what I implemented which works and is responsive to the two different breakpoints. -->

## Author

- LinkedIn - [RJ Crowder-Schaefer](https://www.linkedin.com/in/rjcrowderschaefer/)
- Frontend Mentor - [@rjcrowderschaefer](https://www.frontendmentor.io/profile/rjcrowderschaefer)
- GitHub - [@rjcrowderschaefer](https://github.com/rjcrowderschaefer)