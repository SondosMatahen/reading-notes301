# Read 5
<hr>
<br>

## Node.js For Beginners. Deploy Your Blog to Heroku

we will build a simple web server . We will use Node.js as a server part technology for that task. Then we'll use Heroku cloud application platform to turn this local server into a world wide server.
<br>

* Node.js is an open source, cross-platform runtime environment, which allows you to build server-side and networking applications. It's written in JavaScript and can be run within the Node.js runtime on any platform.
<br><br>
Works fine. But it works locally. WWW is for "World Wide Web" and we will turn your local server into a world wide server. We'll use Heroku cloud application platform for this. Heroku is a cloud platform as a service (cool long-bearded programmer guys call such type of things "PaaS"). It allows you to deploy your web server, so everyone could see how awesome you are as a web developer.

<br><br>
var http = require("http"); will give the key to Node’s HTTP functionality

var fs = require("fs"); for possibility to interact with the file system

var path = require("path"); allows you to handle file paths

var mime = require("mime"); allows you to determine a file’s MIME-type it’s not a part of Node.js
<br>

## It's Heroku time!
Open your terminal within your project folder. 
* Then run: git init
* We'll create our first Heroku application now: heroku create
* Everything is done. You can try it now: heroku open 

<br><br>
<br><br>


you can combine Node.js with different technologies, such as CSS3 and HTML5, then spice it with some JavaScript functionality. There is really a lot of libraries and frameworks to take a look at. Personally I started to dig into Webix, it's a relatively new library and is developed by a small software company from Eastern Europe. Samples of apps made with the library and Node.js: CRM and task planner. Seems like you can create anything with the right client-side framework and Node.js.