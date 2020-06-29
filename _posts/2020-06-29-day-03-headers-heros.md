---
title: "Day 3: Page Headers and Hero Sections"
date: 2020-06-29T08:00-03:00
categories:
  - schedule
toc: true;
tags:
  - html
excerpt: Home pages often have large hero sections to grab the user's attention. Internal pages will often have a simpler page header.
---
## Reminders for Tony
1. Put on mic
2. Open Zoom chat
3. Record! Anyone else?

## Prep
- [Document and Website structure](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Document_and_website_structure)
- [Backgrounds and borders](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Backgrounds_and_borders)
- Videos by Jen Simmons
  - [Introduction to Viewport Units](https://youtu.be/_sgF8I-Q1Gs)
  - [Designing for a Viewport](https://youtu.be/QY3lTBZnJmE)
  - [Unlocking the Power of CSS Overrides – 4/7 Resilient CSS](https://youtu.be/0X6zrW2QW8Q)
- Flexbox
  - Summary: [Complete Guide to Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
  - Game: [Flexbox Froggy](https://flexboxfroggy.com/)
  - Game: [Flexbox Zombies](https://geddski.teachable.com/p/flexbox-zombies)

## Lecture/Live-code: Page structure
Discussion: common page sections and their corresponding *semantic* elements:
- `header`
- `nav`
- `main`
- `section`
- `article`
- `aside`
- `footer`

### Live-code: Header section
Continuing with your project, we'll expand on our text-centric page (which could be a blog post, about page, etc) and begin building our page header.

#### Objectives
1. Add a company/organization/website name ([Tony's random band name generator](https://acidtone.github.io/namor/)) inside a new `header` above your content.
2. Add a coloured background to the `header` element using the `background-color` property.
3. Change the colour of the company name using the `color` property (while ensuring proper colour contrast).
4. Optional: 
    - Change your title text with `font-variant: small-caps`. What other effects can to implement?
    - Enhance the background of your header with `linear-gradient()`.
    - Add a logo as an HTML image ([example](https://acidtone.github.io/images/bt-logo.svg)) to the left of the page title (don't forget: `img` elements are `inline` by default).

### Activity: Make your own header section
You will be working in pairs. 
- Find examples of page headers online.
- What are some of the design patterns (conventions) you're seeing? Can any be incorporated into your design?
- Using the knowledge (and code) you've gained from the live-code session, try making your own header section. Start with the bare minimum (page title with colouring) and try adding some design elements that you've found online.

## Lecture: From header to hero section
Header sections are fine for internal pages (or home pages 10-15 years ago) but the convention for landing pages is the hero section.

Discussion: three technologies will help us make big and bold hero sections that will grab the user's attention:
- Viewport units
- CSS images
- Flexbox

### Live-code: A basic hero section 
Let's turn our header section into a hero section.

#### Objectives
1. Using viewport units, we'll expand the height of the `header` element so that it covers more than 50% of the page.
2. Use the following properties (and Lorem Picsum) to add a background image to your `header` section:
    - `background-image`
    - `background-size`
    - `background-position`
3. Using Flexbox, position (and `color`) your text on the background image so that the text is readable.
    - What element will serve as your container?
    - What direction does `justify-content` affect, by default? `align-items`?
    - What width does your title need to be? Is the default (100%) good enough?

### Activity: Adapt your header section into a hero section
You will be working in pairs. Start a new codepen based on your header page (or start fresh) so you have a copy for both home and internal pages.
- Are there any other ways of increasing the size of the `header` besides using the `height` property?
- Try using a `linear-gradient()` with the CSS background image to achieve different effects.
- When using Flexbox pay careful attention to the container/item relationship.

## Mid-day Huddle
- who needs help?
- any pivots?
- any show-and-tell?

[*lunch*]

## Code Walk-through
- what did we learn?
- real-world example?

[*break*]

## Activity 2: Optimize and extend
- paired or team?
- How can your code be cleaned up?

## Summary
- any trophies?
- prep for tomorrow?
- applause