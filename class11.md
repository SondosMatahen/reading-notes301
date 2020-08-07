# Read 11
<br>
<hr>
<br>

## EJS
* EJS is a simple templating language that lets you generate HTML markup with plain JavaScript. No religiousness about how to organize things. No reinvention of iteration and control-flow. It's just plain JavaScript.
* to get start with EJS  we should make `npm init -y` then `npm install --save express body-parser corse ejs` 
* package.json will hold our Node application information and the dependencies we need (express and EJS). server.js will hold our Express server setup, configuration. We'll define our routes to our pages here.
* We also have to set EJS as the view engine for our Express application using app.set('view engine', 'ejs');. 
* It is important to note that res.render() will look in a views folder for the view. So we only have to define pages/index since the full path is views/pages/index.
* Using Partials The syntax to use an EJS partial is: <% include FILENAME %>. The path to the partial is relative to the current file.
* we can send data inside view bu res.render('path',{data}).
* Single Variable ,To echo a single variable, we just use <%= tagline %>
* Looping Over Data ,To loop over our data, we will use .forEach
<br><br>

* you can perform a volumes search by sending an HTTP GET request to the following URI: `https://www.googleapis.com/books/v1/volumes?q=search+terms`
* q - Search for volumes that contain this text string. There are special keywords you can specify in the search terms to search in particular fields.
