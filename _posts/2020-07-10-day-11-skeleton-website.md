---
title: "Day 11: Creating a Skeleton Website"
date: 2020-07-10T08:00-03:00
categories:
  - schedule
tags:
  - 
toc: true
excerpt: Now that we have Node, NPM and Express installed on our machines, let build a skeleton website.
---
## Reminders for Tony
1. Put on mic
2. Open Zoom chat
3. Record! Anyone else?

## Topics Covered
- [Express Tutorial: The Local Library website](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs/Tutorial_local_library_website)
- [Express Tutorial Part 2: Creating a skeleton website](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs/skeleton_website)

## Goal for the day
By the end of the day, you should have an Express web server (running on port 3000) statically serving your travel website.

## Topic 1: The Big Picture
Before we dig into the details, we'll take a look at the big picture from frontend to backend and everything in the middle:

### Activity objectives: 
Pull a new version of the [`sample-code`](https://github.com/cprg210/sample-code/) repository:

1. You'll find an example sample website at `/backend/static-express`. Copy this directory into your own working folder.
2. On the command line navigate to your new directory and install the dependencies:

```shell
$ npm install
```

3. Now that your dependencies are installed, let's start up the server:

```shell
$ node app.js
```

4. Checkout the website at `localhost:3000`. You'll be migrating your travel website into this project.

## Topic 2: Functions in-depth
We will chat about proper terminology when using and discussing functions. See the sample files in the sample-code repo at `/_js/functions`.

## Mid-day Huddle
- who needs help?
- any pivots?
- any show-and-tell?

[*lunch*]

### Activity objectives: Separation of concerns
In this activity you will migrate the current version of your travel website into the static-express project:
1. Move your website into the `/public` directory.
2. Start the server to confirm your website is displaying correctly.
3. Separate your css, js and images into the appropriate directories. Your HTML should NOT have any *embedded* CSS (i.e. in a `<style>` element) or JS (i.e. in a `<script>` element)

You are done for the day once you have your code separated and working correctly at `localhost:3000`;

## Open workshop time and Q&A

## Summary
- any trophies?
- prep for tomorrow?
- applause