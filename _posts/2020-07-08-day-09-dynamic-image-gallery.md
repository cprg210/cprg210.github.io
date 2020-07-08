---
title: "Day 9: Dynamic Image Gallery with JS Loops"
date: 2020-07-09T08:00-03:00
categories:
  - schedule
tags:
  - 
toc: true
excerpt: Expanding on what we learned yesterday, we will add Lorem Picsum images to a gallery using a loop.
---
## Reminders for Tony
1. Put on mic
2. Open Zoom chat
3. Record! Anyone else?

## Housekeeping
- Daily Schedule Update:
  - Lunch: 11am-12:30pm
  - End of day: 2pm
- If you need extra help:
  - There will be an open question period from 11-11:30am and 2-2:45pm.
  - Tony will also be available for one-on-one sessions weekday evenings and Saturday afternoons. DM him in Discord to set up an appointment.

## Topics covered
- [Arrays](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/Arrays)
- [Looping code](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Looping_code)
- [Object basics](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/Basics)

## Goal for the day
By the end of the day, you should have a gallery that is dynamically built from an array using a loop.

## Topic 1: Creating an array
Arrays are generally described as "list-like objects"; they are basically single objects that contain multiple values stored in a list. For today's activities we'll be using an array to display an image gallery.

We will be using the following sample code and images:

[Gallery starter code](https://github.com/cprg210/sample-code/tree/master/gallery-starter)

### Activity objectives:
1. Using the sample Javascript code listed above, create a simple array containing the image IDs listed in [`gallery.js`](https://github.com/cprg210/sample-code/blob/master/gallery-starter/gallery.js).

    ```js
      const images = [237, 433, ...];
    ```

2. Using `Element.innerHTML` display a random [Lorem Picsum](https://picsum.photos/) image (250px x 250px) on a web page using the following format:

    ```html
      <img src="https://picsum.photos/id/:imageId/250/250" alt="Random Lorem Picsum">
    ```

## Topic 2: Looping through an array
Programming languages are very useful for rapidly completing repetitive tasks, from multiple basic calculations to just about any other situation where you've got a lot of similar items of work to complete. Here we'll use a loop structure to generate a list of HTML images.

[Looping basics](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Looping_code)

### Activity objectives: 
1. Using the array created earlier and a `for` loop (or similar), log each image Id to the console.
2. Using that same loop, generate a list of HTML images and add them to a web page using `Element.innerHTML`.
    - hint: Javascript has an *addition assignment* operator that might help you glue strings together.
4. Use `splice()` to show a subset of the image list (similar to a paginated web page).

## Mid-day Huddle
- who needs help?
- any pivots?
- any show-and-tell?

[*lunch*]

## Topic 3: Adding meta information to our gallery
Our array of image IDs gets the job done but it would be nice to have more descriptive `alt` text. For this, we need more complex data structures.

### Activity objectives
1. Refactor your array of image IDs to include the `title` from our original [source list](https://github.com/cprg210/sample-code/blob/master/gallery-starter/gallery.js). Instead of an array of numbers (the image IDs) use an array of arrays to include `title` as a second item for each image.

    ```js
    const images = [
      [237, 'Puppy'],
      [433, 'Bear'],
      ...
    ]
    ```
2. Refactor your HTML gallery to include the `title` as custom `alt` text for each image:

    ```html
    <img src="https://picsum.photos/id/:imageId/250/250" alt="[title]">
    ```
3. Try adding the `fileName` to your new array and link your images locally using the [source files](https://github.com/cprg210/sample-code/tree/master/gallery-starter/images) provided.

## Summary
- any trophies?
- prep for tomorrow?
- applause