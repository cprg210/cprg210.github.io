---
title: "Day 14: Controllers and JSON Endpoints"
date: 2020-07-15T08:00-03:00
categories:
  - schedule
tags:
  - 
toc: true
excerpt: The real power of Express comes with custom routes and controllers. In industry, we call these API Endpoints.
---
## Reminders for Tony
1. Put on mic
2. Open Zoom chat
3. Record! Anyone else?

## Topics Covered
1. Introduction to JSON and JSON APIs
    - MDN: [Working with JSON](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/JSON)
    - [JSON Placeholder](https://jsonplaceholder.typicode.com/)
2. Asynchronous Javascript basics
    - [Graceful asynchronous programming with Promises](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Asynchronous/Promises)
    - [`response.json` Documentation](https://expressjs.com/en/api.html#res.json)
3. Consuming JSON APIs with `fetch()`
    - [Using fetch()](https://css-tricks.com/using-fetch/)
    - [Express Tutorial Part 4: Routes and controllers](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs/routes)

## Goal for the day
By the end of the day, you'll have migrated a frontend javascript array to a Node custom model on the backend.

- [Today's finished code](https://github.com/cprg210/sample-code/tree/master/backend/4-animals-json-fetch)

## Topic 1: JSON APIs
[JavaScript Object Notation](https://developer.mozilla.org/en-US/docs/Glossary/JSON) (JSON) is a standard text-based format for representing structured data based on JavaScript object syntax. It is commonly used for transmitting data in web applications (e.g., sending some data from the server to the client, so it can be displayed on a web page, or vice versa). You'll come across it quite often, so in this article we give you all you need to work with JSON using JavaScript, including parsing JSON so you can access data within it, and creating JSON.

### Activity objectives: Postman setup
1. [Download and install Postman][https://www.postman.com/downloads/] ([Getting started](https://learning.postman.com/docs/getting-started/introduction/))
2. Using Postman, explore this list of open JSON APIs. Are there any that could be used in your group project?
3. Try submitting a POST request (with data) to the [JSON placeholder](https://jsonplaceholder.typicode.com/) `/posts` endpoint.

## Topic 2: Asynchronous Javascript basics
[Promises](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise) are a comparatively new feature of the JavaScript language that allow you to defer further actions until after a previous action has completed, or respond to its failure. This is useful for setting up a sequence of async operations to work correctly. This article shows you how promises work, how you'll see them in use with web APIs, and how to write your own.

### Activity objectives: Create a `GET /api/destinations` endpoint
1. Make sure you have a valid Destinations module included in your project using `require()`.
2. Using the `response.json` method, create a `GET /api/destinations` endpoint in Express that returns the correct Destinations items for your frontend loop to work.

## Mid-day Huddle
- who needs help?
- any pivots?
- any show-and-tell?

[*lunch*] 

## Topic 3: Consuming JSON APIs with `fetch()`
The [Fetch API](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API) provides a JavaScript interface for accessing and manipulating parts of the HTTP pipeline, such as requests and responses. It also provides a global fetch() method that provides an easy, logical way to fetch resources asynchronously across the network.

### Activity objectives: Gallery refactor
It's time to refactor your Destinations gallery loop.
1. Instead of feeding your loop with a local data model (i.e. your image array), set up an asynchronous `fetch()` call that requests the data from your server instead.
2. What other JSON API endpoints might come in handy for your project?

## Summary
- any trophies?
- prep for tomorrow?
- applause