# Read 9
<br>
<hr>
<br>

## Concepts of Functional Programming in Javascript
* “Complexity is anything that makes software hard to understand or to modify." — John Outerhout
* Functional programming is a programming paradigm — a style of building the structure and elements of computer programs — that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data.
* pure function: It returns the same result if given the same arguments (it is also referred as deterministic)
It does not cause any observable side effects.
* Any function that relies on a random number generator cannot be pure.
* Pure functions are stable, consistent, and predictable. Given the same parameters, pure functions will always return the same result. We don’t need to think of situations when the same parameter has different results — because it will never happen.
* pure functions + immutable data = referential transparency
* Functions as first-class entities can: refer to it from constants and variables ,pass it as a parameter to other functions,return it as result from other functions
<br><br>

* Higher-order functions:
When we talk about higher-order functions, we mean a function that either:
takes one or more functions as arguments, or
returns a function as its result
<br><br><br>

* Refactoring JavaScript for Performance and Readability :
  1. Scenario 1:
   We're an URL-shortening website, like TinyURL. We accept a long URL and return a short URL that forwards visitors to the long URL. We have two functions.
   `
const URLstore = [];

function makeShort(URL) {
  const rndName = Math.random().toString(36).substring(2);
  URLstore.push({[rndName]: URL});
  return rndName;
}

function getLong(shortURL) {
  for (let i = 0; i < URLstore.length; i++) {
    if (URLstore[i].hasOwnProperty(shortURL) !== false) {
      return URLstore[i][shortURL];
    }
  }
} `

2. Scenario 2
We're a social media website where user URLs are generated randomly. Instead of random gibberish, we're going to use the friendly-words package that the Glitch team works on. They use this to generate the random names for your recently created projects!
`
const friendlyWords = require('friendly-words');

function randomPredicate() {
  const choice = Math.floor(Math.random() * friendlyWords.predicates.length);
  return friendlyWords.predicates[choice];
}

function randomObject() {
  const choice = Math.floor(Math.random() * friendlyWords.objects.length);
  return friendlyWords.objects[choice];
}

async function createUser(email) {
  const user = { email: email };
  user.url = randomPredicate() + randomObject() + randomObject();
  await db.insert(user, 'Users')
  sendWelcomeEmail(user);
} `


