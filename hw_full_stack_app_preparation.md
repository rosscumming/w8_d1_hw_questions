# Homework: Full Stack Games Hub App

### Learning Objectives

- Understand the relationship between client, server and database
- Be able to navigate a codebase that you haven't written

## Brief

Your boss has asked to you look over the codebase of a full-stack JavaScript application. The front-end is written in JavaScript using Vue, the back-end uses an Express server and a MongoDB database. Your task is to make yourself familiar with the codebase.

The application includes a README.md with instructions on running the application.

![Overview of the tech stack and tooling with commands](images/tech_stack_with_commands.png)

## MVP

### Task

Draw a diagram showing the dataflow through the application starting with a form submission, ending with the re-rendering of the page. This will involve a multi-direction data-flow with the client posting data to the server and the server sending data back to the client with the response. Detail the client, server and database in the diagram and include the names of the files involved in the process.

### Questions

1. What is responsible for defining the routes of the `games` resource?
```
games router using function which is defined in create router

```

2. What do you notice about the folder structure?  Whats the client responsible for? Whats the server responsible for?

```
clients responsible for views and rendering of how how the app looks. the server is responsible for the database.
```
3. What are the the responsibilities of server.js?


```
server.js connects to the database and listen to port 3000 to set up the web server. also creates gamesRouter which contains the restful routes

```
4. What are the responsibilities of the `gamesRouter`?

```
gamesRouter provides a standard set of restful routes  for all games in gamesCollection (CRUD methods)
```
5. What process does the the client (front-end) use to communicate with the server?

```
GamesService.js sets the base route to be used in the functions within this file when they are fetched. this is listened on localhost:3000 by the server.

```

6. What optional second argument does the `fetch` method take? And what is it used for in this application? Hint: See [Using Fetch](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch) on the MDN docs

```
the fetch method can take an initial object that allows you to control a number of different settings.

```

7. Which of the games API routes does the front-end application consume (i.e. make requests to)?

```
the games API routes consumes the 3 methods within gamesservices.js to create, read, and delete (minus update)
```

8. What are we using the [MongoDB Driver](http://mongodb.github.io/node-mongodb-native/) for?

```
MongoDB driver allows us to connect and manipulate the data from a database

```

## Extension

Why do we need to use [`ObjectId`](https://mongodb.github.io/node-mongodb-native/api-bson-generated/objectid.html) from the MongoDB driver?

Add to your diagram the dataflow for removing a game.
