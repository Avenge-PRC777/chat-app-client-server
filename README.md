# chat-app-client-server
A basic chat application to understand client-server architecture

Table of Contents
=================

   * [chat-app-client-server](#chat-app-client-server)
   * [Table of Contents](#table-of-contents)
   * [Client-Server Architecture](#client-server-architecture)
      * [What is front-end and back-end?](#what-is-front-end-and-back-end)
      * [What are the types of webapps?](#what-are-the-types-of-webapps)
      * [How do real time web apps function?](#how-do-real-time-web-apps-function)
      * [What is ExpressJS and Socket IO?](#what-is-expressjs-and-socket-io)
   * [Getting Started](#getting-started)
   * [Deploying](#deploying)

# Client-Server Architecture

## What is front-end and back-end?

- **Front End** is the part of website that user/client directly interacts with;
  + It may be images, tables, buttons, menu;
  + It should be **responsive** that is appear correctly on devices of all sizes(no abnormal behaviour);
  + Front end languages: **HTML, CSS, JavaScript**;
  + HTML and CSS deal with styling and designing(the look);
  + JS deals with the functionalities(for eg. click on button or arrow keys pressed in a JS game);
  + Front end extensions: AngularJS, React.js, jQuery, SASS, Bootstrap;
  + Angular JS is a framework used to make Single page web apps, React.js is a JS library to create UI

- **Back End** is the part that handles server side;
  + Tasks like storing data in a database, calling APIs;
  + Client has no control over it, only server side programmers;
  + Back end languages: **PHP,JavaScript(Yes),Node.js, Python, REST, Ruby**;
  + Node.js is **runtime environment** to execute JS code outside a browser(for eg. to run HelloWorld.js,i.e to see output, use node);
  + Back end frameworks: **Express**, Django, Spring;

## What are the types of webapps?

- There are three kinds of web products
  + **Static Websites**: show static pages to all;
  + **Webapp**: pages shown are different for clients(customized to client data);
  + **Traditional webapps**:client has to ask from server information/data;
  + **Real time webapps**:information is transmitted almost instantaneously between users and servers(between users too);
  + For eg. a chat application between two clients, where chat goes to server and a client has to poll to get updates;
  + Basically, real time webapp is about dealing with state of server, Facebook is also a good example, as real time notifications come to you;

## How do real time web apps function?

- Most of the internet works on **HTTP Request/Response model**;
  + It means client sends request for data and server sends response;
  + It also implies that the protocol is client oriented and **server can't send any data to client over HTTP without a request**;
  + Let us say our model M consists of client A and B and server S;
  + Say A requested S for an image and got the response, but then B sent an urgent updated image to server. To let A know of such real time changes, the following techniques are available.
- **User Driven** technique: User swipes down or presses refresh button, on doing so a request is sent to server, which sends updated data; 
- **Polling** technique: Known as *client pull*, it is of three types-
  + **Short Polling**: Every T seconds(a small interval) the client sends a request to server, the server responds with data(if updated);
  + This a waste of resources on server as server has to allocate resources for request and carry operations for response, which may not even contain updated data;
  + It also increases traffic with more clients.
  + **Adaptive Polling**: Client increases checking time from T to 2T, 4T, 8T,... if it does not receive updates;
  + When it does, it switches back to a smaller polling interval again;
  + **Long Polling**: Instead of responding without updates, server now holds on to the HTTP request until an update;
  + After it responds with the update, the client sends a request to the server that it hold on to again and the cycle continues;

![](https://raw.githubusercontent.com/Avenge-PRC777/chat-app-client-server/master/images/polling.png)

> Long Polling

- **Websocket** technique: It is a HTTP based protocol;
  + Client requests server to upgrade connection protocol from HTTP to websocket;
  + Websocket connection is **bidirectional** and server can push data without requests;
  + Downsides-one has to check if connection went down and client missed any update, more ever websocket is heavy on server with respect to performance, so supports less number of clients.

![](https://raw.githubusercontent.com/Avenge-PRC777/chat-app-client-server/master/images/websocket.png)

> Websocket

## What is ExpressJS and Socket IO?

![](https://raw.githubusercontent.com/Avenge-PRC777/chat-app-client-server/master/images/express.png)

> Express JS

- Express is an open source JavaScript framework to create web apps;
- It is used for building web applications and APIs.
- It is **de facto** standard server framework for Node.js that means it is the most widely used framework for server side login in JS;

![](https://raw.githubusercontent.com/Avenge-PRC777/chat-app-client-server/master/images/socketio.png)

> Socket.IO

- Socket is a JavaScript library that helps in upgrading connection to WebSocket if possible or downgrading to HTTP Polling;
- It is most widely used for real time web apps to enable bidirectional communication;
- It has a client side library that run in browser and server side library for Node.js;
- Server side library integrates with HTTP server-socket.io, whereas client library loads on browser-coket.io-client;
- For development socket.io serves client automatically;

# Getting Started

## All about Node.JS

- **Installing Node.js**: It is recommended that one install virtualenv for python, create a python 2.7 virtual environment named as nodejs\_environments, and do **pip install nodeenv**;
  + **nodeenv** is used to create virtual environments for nodejs projects;
  + Like python virtual environment has its own python and pip version and does not use system ones, nodeenv makes a separate node and npm;
  + Use **source nodeJSEnvironments/projectname/bin/activate** to activate the nodeenv and **deactivate\_node** to deactivate it;
  + Always check *node and npm version and location* using **--version** and **which npm** or **which node**;
- **Node project configuration**: Your node project should always have a **package.json** file
  + **package.json** file contains directives for **npm**, the two compulsory ones are **name and version**;
  + Optional directives are **description and dependencies**,dependencies will contain other modules you use for your module(project);
  + **npm install module@version** will fill dependencies automatically with the module;
- Node follows **semantic versioning** that is majorVersion.minorVersion.patchVersion
  + When someone clones your repo and does **npm install** to install the dependencies, he/she will get latest minorVersion(because of ^ in package.json);
  + Future version of a module can break your code, so here comes **package-lock.json**, npm looks into it and ignores the '^' and installs owner's(original) version


# Deploying
