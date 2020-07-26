# Read 7
<br>
<hr>
<br>

 ## Rest
* REST provides a definition of a “resource”, which is what those things point to.
* Every programming language, database, or other kind of system has a different way of talking about nouns. That's why the URL is so important. It let's all of these systems tell each other about each other's nouns.
* here's a powerful concept in programming and CS theory called “polymorphism”. That's a geeky way of saying that different nouns can have the same verb applied to them.
* f a system wants to replace something in another system, it uses an HTTP PUT, or, to do a partial update, it'll hopefully use PATCH.

<br><br>

## Request basics
* A request can be initiated by invoking the appropriate method on the request object, then calling .then() (or .end() or await) to send the request. For example a simple GET request:
`request
   .get('/search')
   .then(res => {
      // res.body, res.headers, res.status
   })
   .catch(err => {
      // err.message, err.response
   });`

* `request('GET', '/search').then(success, failure);` HTTP method may also be passed as a string:
* `request('GET', '/search').end(function(err, res){
  if (res.ok) {}
});` Old-style callbacks are also supported, but not recommended. Instead of .then() you can call .end()
* DELETE, HEAD, PATCH, POST, and PUT requests can also be used, simply change the method name: `request
  .head('/favicon.ico')
  .then(res => {

  });`
