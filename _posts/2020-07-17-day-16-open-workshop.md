---
title: "Day 16: Open Workshop Day"
date: 2020-07-17T08:00-03:00
categories:
  - schedule
tags:
  - 
toc: true
excerpt: The last day of this course will be dedicated to cleaning up our projects, working on the final assignment and preparing for PROJ 207
---
## Reminders for Tony
1. Put on mic
2. Open Zoom chat
3. Record! Anyone else?

## Topics Covered
- [How to host a RESTful Node.js server with MongoDB Atlas database on Heroku](https://dev.to/cpclark360/how-to-host-a-restful-node-js-server-with-mongodb-atlas-database-on-heroku-1opl)
- [Express Tutorial Part 7: Deploying to production](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs/deployment)

## Goal for the day
Last day of class! By the end of the day, you should have your Travel Experts website fully deployed to Heroku/Atlas.

If we have time, we'll build a POST endpoint for handle form data.

## Topic 1: Final assignment
[New Assignment Breakdown](https://github.com/cprg210/assignments/)

### Activity objectives: Deploying your app to Heroku/Atlas
#### Heroku
1. `$ npm install heroku`
2. Add start script - Heroku needs to know what command to fun to start your server (i.e. `node app.js` or similar). This is added to your `package.json` file. 

    ```json
    "scripts": {
      "test": "echo \"Error: no test specified\" && exit 1",
      "start": "node app.js"
    }, 
    ```
3. Push your repo to a public GH repository
4. New -> Creat New App
5. Deployment method -> Connect to Github and select your source repository and Connect.
6. "Heroku dashboard > Select your server App > Settings > Reveal Config Vars"
    - add Atlas connection string
7. Deploy branch
8. Done!

If you see and "Application Error" for your depolyed site, check the logs: `heroku logs --tail -a [container-name]`.
{: .notice--warning}

#### Frontend
1. Change `fetch()` URL from `http://locahost:3000/api/desinations` to `http://[container-name].herokuapp.com/api/desinations`.
2. `npm install cors` - Heroku needs to add CORS header (based on our code)

    ```js
    // cors origin URL - Allow inbound traffic from origin
    corsOptions = {
      origin: "https://dashboard.heroku.com",
      optionsSuccessStatus: 200 // some legacy browsers (IE11, various SmartTVs) choke on 204
    };
    app.use(cors(corsOptions));
    ```



## Topic 2: POST endpoints? - Justice for jellyfish

## Mid-day Huddle
- who needs help?
- any pivots?
- any show-and-tell?

[*lunch*]

### Activity objectives: 

## Summary
- any trophies?
- prep for tomorrow?
- applause