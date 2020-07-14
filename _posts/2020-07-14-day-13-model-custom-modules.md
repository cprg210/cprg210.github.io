---
title: "Day 13: Models, Routes and Custom Modules"
date: 2020-07-14T08:00-03:00
categories:
  - schedule
tags:
  - 
toc: true
excerpt: Let's copy our Animal data (our model) from our frontend Javascript app to a Node custom module. Also, it turns out Tony still likes EJS over Pug.
---
## Reminders for Tony
1. Put on mic
2. Open Zoom chat
3. Record! Anyone else?

## Topics Covered
1. EJS quickie
    - [EJS home page](https://ejs.co/)
    - [EJS tag reference](https://www.npmjs.com/package/ejs#tags)
2. Model fixtures with`require()` and `module.exports`
    - [Model-View-Controller](https://developer.mozilla.org/en-US/docs/Glossary/MVC)
    - [Function scope example](https://github.com/cprg210/sample-code/blob/master/_js/functions/4-scope.js)
    - [Requiring modules in Node.js: Everything you need to know](https://www.freecodecamp.org/news/requiring-modules-in-node-js-everything-you-need-to-know-e7fbd119be8/)
3. Dynamic endpoint handlers with `request.params`
    - [Express Tutorial Part 4: Routes and controllers](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs/routes)
    - [Understanding the req Object in Express.js](https://www.digitalocean.com/community/tutorials/nodejs-req-object-in-expressjs)
    - [request.params](https://expressjs.com/en/api.html#req.params)

## Goal for the day
We'll start the day with a long list of animal endpoint handlers. By the end of the day, we should have all animal pages served with one endpoint (`GET /:id`).
- [Starter code for today](https://github.com/cprg210/sample-code/tree/master/backend/2-animals-ejs)
- [Today's finished code](https://github.com/cprg210/sample-code/tree/master/backend/3-animals-custom-module)

## Topic 1: EJS quickie
We will discuss the EJS alternative to Pug. While Pug has some great features, it can be difficult to create page partials, so we will quickly walk through the example from yesterday using EJS.

- [EJS home page](https://ejs.co/)
- [EJS tag reference](https://www.npmjs.com/package/ejs#tags)

### Activity objectives

## Topic 2: Model fixtures with `require()` and `module.exports`
We will discuss the model in deeper detail. 
- [Model-View-Controller](https://developer.mozilla.org/en-US/docs/Glossary/MVC)
- [Function scope example](https://github.com/cprg210/sample-code/blob/master/_js/functions/4-scope.js)
- [Requiring modules in Node.js: Everything you need to know](https://www.freecodecamp.org/news/requiring-modules-in-node-js-everything-you-need-to-know-e7fbd119be8/)

## Mid-day Huddle
- who needs help?
- any pivots?
- any show-and-tell?

[*lunch*]

### Activity objectives

## Topic 3: Dynamic endpoint handlers with `request.params`
See: 
- [Express Tutorial Part 4: Routes and controllers](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs/routes)
- [Understanding the req Object in Express.js](https://www.digitalocean.com/community/tutorials/nodejs-req-object-in-expressjs)
- [request.params](https://expressjs.com/en/api.html#req.params)

### Activity objectives
1. Using [today's finished code](https://github.com/cprg210/sample-code/tree/master/backend/3-animals-custom-module), refactor the `GET /:id` endpoint so that it uses the animal `title` instead.

## Summary
- any trophies?
- prep for tomorrow?
- applause