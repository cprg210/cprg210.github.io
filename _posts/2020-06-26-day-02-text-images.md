---
title: "Day 2: Web Typography and Floated HTML Images"
date: 2020-06-26T08:00-15:00
categories:
  - schedule
tags:
  - css
excerpt: Now that we have some HTML work with, we'll begin styling the text, insert an image or two and add a top bar.
---
## Reminders for Tony
1. Put on mic
2. Open Zoom chat
3. Record! Anyone else?

## Topics Covered
- Video: [Introduction to Viewport Units](https://www.youtube.com/watch?v=_sgF8I-Q1Gs)
- HTML
  - [Creating hyperlinks](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Creating_hyperlinks)
  - [Document and Website structure](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Document_and_website_structure)
  - [Images in HTML](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Images_in_HTML)
- CSS 
  - [Type, class, and ID selectors](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Selectors/Type_Class_and_ID_Selectors)
  - [Sizing items in CSS](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Sizing_items_in_CSS)
  - [Images, media and form elements](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Images_media_form_elements) (you can stop at "Form Elements")
  - [Backgrounds and borders](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Backgrounds_and_borders)
  - [Styling text](https://developer.mozilla.org/en-US/docs/Learn/CSS/Styling_text)
- Summary: [Complete Guide to Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
- Game: [Flexbox Froggy](https://flexboxfroggy.com/)
- Find some Lorem Picsum links that speak to you:
  - Aim for images that have a large areas of consistent colour/contrast

## Goals
- what will we have to show for it at the end of the day? We will take the blog post from yesterday and then:
  1. make our text pretty
  2. make it centered
  3. add a page header
  4. turn that header into a hero section
- why should I care?

## Lecture/Live-code: Web typography
### Objectives
Using the text example from yesterday, we will:
- Use the font inspector to investigate the font settings of a website.
- Change the default font.
- Balance `font-size`, line length (`width`) and `line-height`
- Make it minimally responsive with `max-width`

[*break*]

## Activity 1: Brute-force solution
This will be a paired activity.

The "blog post" you create can be on any topic but keep your text readable:
- short paragraphs
- lots of headings
- bulleted or numbered lists where appropriate

## Lecture/Live-code: Floated HTML image
### Objectives
Continuing with your project, try the following:
- Add a 300x300 pixel HTML image to your page using the `img` tag.
- Float your text around the image using the `float` property.
- A *keyline* is a print industry term for the 1px border you sometimes see around an image. Try adding one to your HTML image using the `border` property.
- For fun, make the image look like a [polaroid](https://www.google.com/search?q=polaroid+image) using the `padding` property.
- Try rounding the corners of the image using the `border-radius` property.

[*break*]

## Activity 2: Brute-force a solution
You will be working in pairs.
- Repeat the steps your instructor just demonstrated.
- Can you make a circular image using the `border-radius` property?
- What other image effects do you see online that you'd like to try?

## Mid-day Huddle
- who needs help?
- any pivots?
- any show-and-tell?

[*lunch*]

## Lecture 3: Code Walk-through
See the finished [sample post](https://codepen.io/browsertherapy/pen/JjGJxZP):
- What did we learn?
- What are the best practices
- What can be improved in your code?

### Web Typography
Web typography usually starts with choosing a font pairing for headings and body text:

```css
@import url('https://fonts.googleapis.com/css2?family=Karla&family=Raleway:wght@300;400&display=swap');

/* Font */
body {
  font-family: 'Karla', sans-serif;
}

h1, h2, h3, h4, h5, h6 {
  font-family: 'Raleway', sans-serif;
  font-weight: 300;
}
```

Then we set up the "typography triad": font size, line height (aka. leading) and line length. They all depend on your chosen font family and each other. Typographers coined the term "vertical rhythm" to describe the balance of text to white space on the printed page. The same principles apply here.

```css
  /* browser default is usually 16px */
  font-size: 14px; 
  
  /* browser default is usually 1.2 (other length units allowed). Try for a minimum of 1.5, max should be less than 2 */
  line-height: 1.7; 
  
  /* line length: max for print should be 80-95 characters; */
  /* for web: aim for 25-75ch */ 
  max-width: 60ch;
```

### Layout
Now that our text is balanced, let's get our page balanced by centering the entire text block.

```css
.text-box {
  /* This is centering from the outside of the box. This only works if the centered item is narrower than its parent. */
  margin: auto;
}
```

### Imagery
Floating text around images has been done for centuries. It's fallen out of style online but it's a nice tool to have in your kit.

```css
.image {
  float: left;
}
```

We can make the image circular and float the text to match:

```css
.image {
  border-radius: 50%;
  shape-outside: circle(50%);
}
```

This is assuming the image is square. With other aspect ratios, `border-radius: 50%` will create an ellipse (which can be matched by `shape-outside`).
{: .notice--warning}


[*break*]

## Activity 2: Optimize your code
This will be working in pairs.
- what can be improved?
  - close your tags
  - use quotes for attribute values
  - fix your indentation
  - centre the text in the page with `margin: auto`
  - optional: try floating your text in a circle with `shape-outside`
  - optional: try validating your code with the W3C HTML validator

## Summary
- any trophies?
- prep for tomorrow?
- applause