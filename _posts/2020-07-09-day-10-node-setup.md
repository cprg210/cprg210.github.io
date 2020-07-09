---
title: "Day 10: Setting up Node and NPM"
date: 2020-07-10T08:00-03:00
categories:
  - schedule
tags:
  - 
toc: true
excerpt: We will be following the MDN Express/Mongoose tutorial modules for the server-side component of this course.
---
## Reminders for Tony
1. Put on mic
2. Open Zoom chat
3. Record! Anyone else?

## Topics Covered
- [Express/Node introduction](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs/Introduction)
- [Setting up a Node development environment](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs/development_environment)

## Goal for the day
By the end of the day, you should have Node, NPM and Express Generator installed on your machine. 

**Important:** Copy [this .gitignore file](https://github.com/cprg210/sample-code/blob/master/.gitignore) into any node/express project you are committing to GitHub. This will stop unwanted files (such as the node_modules directory) from being push to your remote repo.
{: .notice--warning}

## Topic 1: Introduction to Node
[Node](https://nodejs.org/) (or more formally Node.js) is an open-source, cross-platform runtime environment that allows developers to create all kinds of server-side tools and applications in JavaScript. The runtime is intended for use outside of a browser context (i.e. running directly on a computer or server OS). As such, the environment omits browser-specific JavaScript APIs and adds support for more traditional OS APIs including HTTP and file system libraries.

See [Introducing Node](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs/Introduction#Introducing_Node)

### Activity objectives: 
See [Installing Node](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs/development_environment#Installing_Node)

## Topic 2: Introduction to NPM
Next to Node itself, [NPM](https://docs.npmjs.com/) is the most important tool for working with Node applications. NPM is used to fetch any packages (JavaScript libraries) that an application needs for development, testing, and/or production, and may also be used to run tests and tools used in the development process. 

## Mid-day Huddle
- who needs help?
- any pivots?
- any show-and-tell?

[*lunch*]

### Activity objectives: 
See [Adding dependencies](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs/development_environment#Adding_dependencies)

## Topic 3: Introduction to Express 
[Express](https://expressjs.com/) is the most popular Node web framework, and is the underlying library for a number of other popular [Node web frameworks](https://expressjs.com/en/resources/frameworks.html). It provides mechanisms to:
- Write handlers for requests with different HTTP verbs at different URL paths (routes).
- Integrate with "view" rendering engines in order to generate responses by inserting data into templates.
- Set common web application settings like the port to use for connecting, and the location of templates that are used for rendering the response.
- Add additional request processing "middleware" at any point within the request handling pipeline.

### Activity objectives: 
See: [Installing the Express Application Generator](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs/development_environment#Installing_the_Express_Application_Generator)

## Summary
- any trophies?
- prep for tomorrow?
- applause