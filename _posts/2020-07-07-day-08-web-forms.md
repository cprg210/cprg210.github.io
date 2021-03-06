---
title: "Day 8: Modifying Page Text with JS and Web Forms"
date: 2020-07-08T08:00-03:00
categories:
  - schedule
tags:
  - 
toc: true
excerpt: Javascript is often used to control web forms. In this session we will modify page text based on form input.
---
## Reminders for Tony
1. Put on mic
2. Open Zoom chat
3. Record! Anyone else?

## Housekeeping
- [Announcing Assignment 2](https://github.com/cprg210/assignments/blob/master/assignment-2/README.md)
- [Course Assessment Schedule](https://github.com/cprg210/assignments/)
- [PROJ 207 Teams](https://github.com/cprg210/assignments/blob/master/proj-207.md)

## Topics Covered
- [Textbook Javascript Overview]({% link _pages/textbook.md %})
- [How to structure a form](https://developer.mozilla.org/en-US/docs/Learn/Forms/How_to_structure_a_web_form)
  - [Form validation](https://developer.mozilla.org/en-US/docs/Learn/Forms/Form_validation)
- [The form submit event](https://developer.mozilla.org/en-US/docs/Web/API/HTMLFormElement/submit_event)
- [`Element.innerHTML`](https://developer.mozilla.org/en-US/docs/Web/API/Element/innerHTML)
  - See also: [HTMLElement.innerText](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/innerText)
  - [What's the difference between `innerText` and `innerHTML`?](https://stackoverflow.com/questions/19030742/difference-between-innertext-and-innerhtml)
  - [What's the difference between `HTMLElement` and `Element`?](https://stackoverflow.com/questions/6581680/whats-the-difference-between-htmlelement-and-element)

## Goal for the day
By the end of the day, you should have a form that can update content on a web page.

[Dynamic Page Text Demo](https://codepen.io/browsertherapy/pen/xxZYemZ)

## Topic 1: Javascript overview
We'll take a tour of the Javascript portion of the textbook and overview the major programming concepts associated with Javascript.

### Live-code objectives: Adding machine
- Create a form with the following fields
  - 2 number inputs
  - submit button
- using a form handler, add the two numbers and display the sum to the console.

## Topic 2: Displaying calculator results on a web page
Using `Element.innerHTML` let's display the result of our calculation on our HTML page.

### Live-code objectives: Printing results
- Add a heading or paragraph to the page containing your form.
- Instead of logging the calculator result to the console, display the data in your new element using `Element.innerHTML`.

## Mid-day Huddle
- who needs help?
- any pivots?
- any show-and-tell?

[*lunch*]

### Activity: Calculator
Extend the adding machine provided in the live code session and add support for subtraction, multiplication and division using a `select` menu.

Supporting materials:
- [Basic math in JavaScript - numbers and operators](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/Math)
- [Making decisions in your code - conditionals](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/conditionals)

## Optional Lecture

### Activity: String concatenation
Using template literals, display a sentence that summarizes the results of the calculator and add it as content of a paragraph element.

`[number 1] [multiplied by|plus|minus|divided by] [number 2] equals [result]`

Supporting materials:
- [Handling text - strings in JavaScript](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/Strings#Concatenating_strings)

## Summary
- any trophies?
- prep for tomorrow?
- applause