# chat-app-client-server
A basic chat application to understand client-server architecture

Table of Contents
=================

   * [chat-app-client-server](#chat-app-client-server)
   * [Technologies Used](#technologies-used)
   * [Client-Server Architecture](#client-server-architecture)
      * [What is front-end and back-end?](#what-is-front-end-and-back-end)
      * [Okay, so what about nature of webapps?](#okay-so-what-about-nature-of-webapps)
   * [Getting Started](#getting-started)

# Technologies Used

![](https://raw.githubusercontent.com/Avenge-PRC777/chat-app-client-server/master/images/express.png)

> Express JS

![](https://raw.githubusercontent.com/Avenge-PRC777/chat-app-client-server/master/images/socketio.png)

> Socket.IO

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
  + Websites: show static pages to all;
  + Webapp: pages shown are different for clients(customized to client data);
  + **Traditional webapps**:client has to ask from server information/data;
  + **Real time webapps**:information is transmitted almost instantaneously between users and servers(between users too);
  + For eg. a chat application between two clients, where chat goes to server and a client has to poll to get updates;
  + Basically, real time webapp is about dealing with state of server, Facebook is also a good example, as real time notifications come to you;

## How do real time web apps function?

- Most of the internet works on **HTTP Request/Response model**;
  + It means client sends request for data and server sends response;
  + It also implies that the protocol is client oriented and **server can't send any data to client without a request**;
- Let us say our model M consists of client A and B and server S;

## What is ExpressJS and Socket IO?



# Getting Started

# Deploying
