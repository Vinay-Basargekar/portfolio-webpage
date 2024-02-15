# Frontend Mentor - Single-page developer portfolio solution

This is a solution to the [Single-page developer portfolio challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/singlepage-developer-portfolio-bBVj2ZPi-x). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)


## Overview
For this challenge, I needed to reproduce a  one-page portfolio website from a Figma design. The design had a mobile, tablet, and desktop layout.The site has links within the page to the contact section as well as links to social media sites.  Although the project links are not to actual projects, the format can be updated and used by anyone interested in displaying projects in this format.

### The challenge

Users should be able to:

- Receive an error message when the `form` is submitted if:
  - Any field is empty
  - The email address is not formatted correctly
- View the optimal layout for the interface depending on their device's screen size
- See hover and focus states for all interactive elements on the page

### Screenshot

![](./images/screenshot-desktop.png)
![](./images/screenshot-tablet.png)
![](./images/screenshot-mobile.png)

### Links

- Solution URL: [Add solution URL here](https://github.com/Stacy-Riley/single-page-developer-portfolio)
- Live Site URL: [Add live site URL here](https://stacy-riley.github.io/single-page-developer-portfolio/)

### Built with

- Semantic HTML5 markup
- CSS
- Flexbox
- CSS Grid
- Mobile-first workflow

### What I learned

Here is the code for the fade affect of the projects in desktop view. I love how it turned out!

```js
portfolioContainers.forEach(container => {
    const projectLinks = container.querySelector(".project-links");
    const imgContainer = container.querySelector(".img-container");

    //EventListener for when mouse enters the ".project" class element in html-desktop only
    container.addEventListener('mouseenter', () => {
        if (window.innerWidth >= 1440) {
            projectLinks.classList.remove('project-links-hide');
            imgContainer.style.opacity = "0.25";
        }
    });

    //EventListener for when mouse leaves the ".project" class element in html-desktop only
    container.addEventListener('mouseleave', () => {
        if (window.innerWidth >= 1440) {
            projectLinks.classList.add('project-links-hide');
            imgContainer.style.opacity = "1";
        }
    });
});
```

### Continued development

I would like to continue to practice position relative and absolute by adding more decorative elements to the sites that I create.  Also, I would also like to use the fade effect found on the projects in the desktop view, larger than 1400px, when the mouse hovered over them.  It would be help solidify the forEach() loop more.

### Useful resources

- [Example resource 1](https://courses.joshwcomeau.com/css-for-js) - The course helped me with the positioning images using position: relative and absolute.
- [Example resource 2](https://developer.mozilla.org/en-US/docs/Web/API/Document/querySelectorAll) - This explained to me that since I used querySelectorAll and have multiple containers, I needed to use forEach() to loop through them and access their inner elements.

## Author

- Website - [Stacy Riley](https://www.createdbystacy.com)
- Frontend Mentor - [@Stacy-Riley](https://www.frontendmentor.io/profile/Stacy-Riley)
- Twitter - [@askstacyriley](https://twitter.com/AskStacyRiley)


