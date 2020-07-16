---
title: "Day 15: Models - Adding a Database with Mongoose"
date: 2020-07-16T08:00-03:00
categories:
  - schedule
tags:
  - 
toc: true
excerpt: We've got a static web server. Let's make it more dynamic by adding a database. While we're at it, let's make it live on Heroku.
---
## Reminders for Tony
1. Put on mic
2. Open Zoom chat
3. Record! Anyone else?

## Topics Covered
1. Introduction to CRUD and Mongoose
    - Search: [SQL vs NoSQL](https://www.google.com/search?q=sql+vs+nosql)
    - Search: [mongoose crud](https://www.google.com/search?q=mongoose+crud)
      - [Mongoose CRUD](https://coursework.vschool.io/mongoose-crud/) (Create, Read, Update, Delete)
2. Mongoose Models
    - [Mongoose Getting Started](https://mongoosejs.com/docs/)
    - [Express Tutorial Part 3: Using a Database (with Mongoose)](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs/mongoose)
3. 

## Goal for the day
By the end of the day, you should have a Destinations model defined in your app using Mongoose. It will be connected to your cloud-hosted Atlas Mongo database.

**Important!** DO NOT push your connection code to a public repository until you learn about environment variables tomorrow. For now, either don't push today's code to Github or make your repository private.
{: .notice--warning}

## Topic 1: Introduction to CRUD
When we are building APIs, we want our models to provide four basic types of functionality. The model must be able to Create, Read, Update, and Delete resources. Computer scientists often refer to these functions by the acronym CRUD. A model should have the ability to perform at most these four functions in order to be complete. If an action cannot be described by one of these four operations, then it should potentially be a model of its own. 

[Source](https://www.codecademy.com/articles/what-is-crud)

### Activity objectives: Setup MongoDB Atlas/Compass
Follow the steps listed in this article: [Using Express with MongoDB Atlas](https://kaloraat.com/articles/how-to-use-mongodb-atlas)

You will need to install two additional Node modules:

```shell
$ npm install dotenv
$ npm install mongoose
```

**MongoDB Connection String** The connection string that you copy and paste from the Connection window in MongoDB Atlas contains `<` and `>` characters. Be sure to remove those when you enter your DB name, username & password.
{: .notice--warning}

When you have completed the steps, your `.env` file should look something like this:

```shell
MONGODB_URL=mongodb+srv://kitten:hello-kitten@cluster0-1c2nl.mongodb.net/animals?retryWrites=true&w=majority
PORT=3000
```

## Topic 2: Mongoose models
For the your Travel Experts project we're going to use the Mongoose ODM to access our library data. Mongoose acts as a front end to MongoDB, an open source NoSQL database that uses a document-oriented data model. A “collection” of “documents” in a MongoDB database is analogous to a “table” of “rows” in a relational database.

This ODM and database combination is extremely popular in the Node community, partially because the document storage and query system looks very much like JSON, and is hence familiar to JavaScript developers.

[Source](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs/mongoose)

## Mid-day Huddle
- who needs help?
- any pivots?
- any show-and-tell?

[*lunch*]

### Activity objectives: Seed database with starting data
In today's sample code folder you will find a `_build.js` file that will insert our "seed data".
1. Navigate to `/sample-code/backend/5-animals-mongoose` in your terminal.
2. Ensure that you have a .env file with your MongoDB Atlas connection string. Note the database that you'll be connecting to (before the "?").
3. Run the build script to import your seed data into your Atlas database.

    ```shell
    $ node _build.js
    ```

4. You should see a new collection in your Atlas control panel. The name will be the plural version of the name you gave your compiled model. For example, the collection name for the animals sample site is "Animals" because the model was compiled with the name "Animal":

    ```js
    module.exports = mongoose.model('Animal', gallerySchema);
    ```

## Topic 3: Exploring Mongoose CRUD operations
If we have time at the end of the day, we'll run through some CRUD examples using Mongoose.

### Activity objectives: Migrate Travel Experts to Atlas
Now that you have a populated database to connect to, it's time to refactor your Travel Experts website to use your new Mongoose model.
1. Refactor `GET /` to use `model.findOne()`;
2. Refactor `GET /api/destinations` to use `model.find()`.

## Summary
- any trophies?
- prep for tomorrow?
- applause