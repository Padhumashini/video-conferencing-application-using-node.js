# video-conferencing-application-using-node.js
Video Call App nodeJS. A Multi user video call and text chat application
# Conference Call
A conference call implementation using WebRTC, Socket.io and Node.js. This demo is ideal for not more than 4 devices.


# Getting Started
- Run `npm ci`
- `cd src`
- `node app.js`


# Features
- Multi-participants
- Toggling of video stream
- Toggling of audio stream (mute & unmute)
- Screen sharing
- Text chat
- Mute individual participant
- Expand participants' stream
- Screen Recording
- Video Recording

to build a video chat app using JavaScript and NodeJS. It will also show you how to use PeerJS, WebRTC, and Socket.io.
Click Here to see live example of the app we’ll be building.
Pre-Project Setup
Here’s what you’ll need:
NodeJS: Visit the official Node.js website to download and install Node.
NPM: NPM program gets installed on your computer when you install Node.js.
Project Setup
All the code for this project can be found in the GitHub Repo
Create an empty directory named video-chat-app.
Open up your console, navigate to our new directory, and run npm init.
Fill out the required information to initialize our project.
Within video-chat-app the directory, and run npm install express ejs socket.io uuid peer. This will install all the dependency that we need to build this application.
And also as a dev dependency, we will install Nodemon. runnpm install — dev nodemon. This will install nodemon as a dev dependency.
Create a file named server.js — this file will keep all our server-side logic
Now that we have our project setup, we can start building!
Creating our Server (with Express JS)
The first thing we need to do is get our server up and running. We’re going to use Express to accomplish this. Express is a minimalist web framework for Node.js — Express makes it very easy to create and run a web server with Node.
Let’s create a boilerplate Express starter app file.
// server.js
const express = require(“express”);
const app = express();
const server = require(“http”).Server(app);
app.get(“/”, (req, res) => {
    res.status(200).send(“Hello World”);
});
server.listen(3030);
Now we have our server running, We can test our server by running:
> nodemon server.js
Now open your browser and visit: localhost:3000 and you should see Hello World.

Creating our first View
Instead of responding with text when someone visits our root route, we’d like to respond with an HTML file. For this, we’ll be using EJS (Embedded JavaScript). EJS is a templating language.
In order to use EJS in Express, we need to set up our template engine. To setup add this line of code in server.js file.
app.set(‘view engine’, ‘ejs’)
EJS is accessed by default in the views directory. Now create a new folder named views in your directory. Within that views folder, add a file named room.ejs. Think of our room.ejs file as an HTML file for now.
Now it’s time to use Socket.io and PeerJS. For those who don’t know Socket.io allows us to do real-time communication. and PeerJS allow us to implement WebRTC.
First, we will import socket.io and peerjs in our server.js file and listen for join-room event.


You can create a free xirsys account and use their free ice server. You can replace the one used with your own at src/assets/js/helpers.js, function getIceServer(). The demo may not work as my xirsys account has been deactivated for reasons best known to them (perhaps the hits were too much) and I am not ready to create a new one. Create yours or look for an alternative.
