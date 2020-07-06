---
title: "Day 7: CSS Toggles with `element.classList`"
date: 2020-07-06T08:00-03:00
categories:
  - schedule
tags:
  - 
toc: true
excerpt: For our first day of Javascript will modify our page styles with the `Element.classList` object.
---
## Reminders for Tony
1. Put on mic
2. Open Zoom chat
3. Record! Anyone else?

## Prep
- Important: [JavaScript Tutorial for Beginners](https://youtu.be/W6NZfCO5SIk) by [Mosh Hamedani](https://codewithmosh.com/)
  - This is an excellent overview of the starter JS concepts you'll need for the rest of this course.
  - There is a handy Table of Contents in the video description.
- Tissue Contrast Illusion: we will be regularly borrowing code from this article for our frontend Javascript lessons.
  - [Browser Therapy Code Challenge](http://browsertherapy.com/challenges/tissue-contrast/)
  - Optional: [Video Walk-through](https://youtu.be/izoeGPX5vfA)
  - [Current Demo](https://acidtone.github.io/illusions/tissue-contrast/)

## Goal for the day
By the end of the day, you should have a button that toggles a CSS class.

[CSS Toggle Demo](https://codepen.io/browsertherapy/pen/BajYPmK)

### Topics Covered
- [Firefox Console](https://developer.mozilla.org/en-US/docs/Tools/Browser_Console)
- JS: ['Element.classList'](https://developer.mozilla.org/en-US/docs/Web/API/Element/classList)
  - [Code Examples](https://developer.mozilla.org/en-US/docs/Web/API/Element/classList#Examples)
- JS: [`Element.addEventListener()'](https://developer.mozilla.org/en-US/docs/Web/API/EventTarget/addEventListener)
  - You will see the keyword `this` used a lot in examples online. For now, avoid the use of `this` until we cover it later in the course. If you just can't wait: [the value of `this` within an event handler](https://developer.mozilla.org/en-US/docs/Web/API/EventTarget/addEventListener#The_value_of_this_within_the_handler)

## Topic 1: Introducing the Document Object Model (DOM) 
When we target an HTML element (ex, a `<p>`) with a new CSS declaration (ex, `color: darkgoldenrod`), we are changing settings of the [Document Object Model](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model). 

### Live-code: Chatting with your browser elf using the Browser Console
In this live-code session, we will explore the Firefox Console (Chrome works too).
- Create an empty HTML file in your editor and view it in a browser.
- Open the Inspector, navigate to the Console and enter the following as separate statements. What does the console return?
  - `"hello world!"` (include the quotes)
  - `4`
  - `1 + 2`
  - `3 / 0`
  - `4 < 5`
  - `innerHeight`
  - `innerWidth`
  - `document`
  - try any other valid js statement

### Activity: Creating a DOM element variable with the `id` attribute
You will be working in pairs. We are going to inspect the body element (of the page we just created) and discover where class names are stored in the DOM.
1. Try entering the following in the console:
    - `body` -> should return an error; "body" doesn't mean anything, yet.
2. Now, add an `id` to `<body>`:

    ```
    <body id="body">
    ```

3. Try repeating Step 1. What happens?
    - `body` -> should now return a DOM element. This means that, simply by giving the element an `id`, **we have created a variable named "body" that references the page's `body` element**. We'll look at better ways to do this later in the course.
    - Try changing the `id` to something other than "body". Does this affect the variable name we need to enter into the console?
    - Notice the triangle next to the returned body element. Click on it and find `classList` in the resulting list. What's its length?
4. Add a class (your choice) to the body tag:

    ```
    <body id="body" class="fancy-bg">
    ```

5. Repeat Step 3 and inspect the body element. How has `classList` changed? What value does `className` hold?
6. Try adding/removing different classes to the `body` tag and re-inspect the element to see how `classList` and `className` changes. What do you think `className` represents?

## Topic 2: Adding and Removing classes with `element.classList`
Using the console, we're going to become more familiar with the `classList` API. `classList` is a Javascript Object, so we need to use [dot notation](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/Basics#Dot_notation) to access the goodies:
- `classList.add()` -> adds a class
- `classList.remove()` -> removes a class
- `classList.toggle()` -> described below
- `classList.contains()` -> returns `true` or `false`
- `classList.replace()` -> rarely used but nice to have

### Live-code objectives
Let's add a class declaration to help us understand `element.classList()` visually. Add this CSS declaration to your page:

```css
.fancy-bg {
  background-color: rebeccapurple;
}
```

Using the console, use the [`classList`](https://developer.mozilla.org/en-US/docs/Web/API/Element/classList) API to:
1. add the class "split-bg" to the `body` element using `classList.add()` (remember the console will accept any valid Javascript statement);
2. remove the same class from the `body` element using `classList.remove()`;
3. toggle the "split-bg" class using `classList.toggle()`.

`classList.toggle()` is a nice shortcut method that saves us from coding a conditional like the following:

```js
// Notice the use of classList.contains(). This method returns true or false; perfect for if/then statements.
if (body.classList.contains("split-bg")) {
  // .split-bg exists so let's remove it...
  body.classList.remove("split-bg");
} else {
  // .split-bg doesn't exist so let's add it...
  body.classList.add("split-bg");
}
```

### Activity: Class action!
Now that you can add/remove/toggle classes that are assigned to an element, add another HTML element (your choice). What other declarations can you define in CSS that you can add/remove as class names using `classList.toggle()` from within the console?

## Mid-day Huddle
- who needs help?
- any pivots?
- any show-and-tell?

[*lunch*]

## Topic 3: Toggling CSS with a `button` event listener
We now know how to add/remove/toggle classes but the console probably isn't the best way to do this. Let's add a button to our page and use it to toggle a class with an event listener.

### Live-code objectives
[Event Listeners](https://developer.mozilla.org/en-US/docs/Web/API/EventTarget/addEventListener) can be added to any element but the `button` is well suited for *click* events.
Copy this sample code ([adapted from this MDN Example](https://developer.mozilla.org/en-US/docs/Web/API/EventTarget/addEventListener#Add_a_simple_listener)) into a `<script></script>` element just before your `</body>` tag):

```js
// Function to toggle a class name
function toggleBackground() {
  body.classList.toggle('fancy-bg');
}

// Add event listener to `button`
btn.addEventListener("click", toggleBackground);
```

### Activity: Hamburger menus
You will work in teams. Now that you know how to toggle CSS at the click of a button, discuss how this technique can be used to toggle a mobile hamburger menu.

Visit your favourite websites on your mobile device. How do they handle navigation on the smaller screen?
- Do they hide the options?
- If so, how do you show the navigation? 
- If it's a hamburger menu, are there any transitions or animations?

## Summary
- any trophies?
- prep for tomorrow?
- applause