
# What is async?

Asynchronous task is a task that can be executed on thethread while another process is running. (So you don't have to wait for something else to finish before executing the task),
Think of washing the dishes or grabbing a cup while boiling a hot water in a kettle we don't need to wait for the kettle to be done boiling before we do the other tasks.


# What is a promise

Promises are a way of handling asynchronous code, specifically for what happens after an asynchronous task is completed.

Promises can only be resolved once if there is more than one resolve in a promise only the first action in the promise will be resolved, the second action in the resolve will do nothing.

We use Promises when working with ajax requests or any async task that requires an action after it has been complete.

# Promise 

A promise conists of three parts, the promise object usually connecting to an api route through a url, .then - what happens after the promise has been resolved, catch - what happens if the promise is rejected.

Writing your own Promise code
```js
 new Promise(function(resolve, reject) {
 resolve('hi);
 resolve('bye);
});
```

Other examples of promise code - Fetch API
```js
fetch('http://example.com/movies.json') 
.then(response => response.data) 
```

# .Then
We know that we are returning a promise when we have to do a .then, which allows us to perform an action with the result when the promise is resolved. .then are asynchonous

```js
axios.get('/api/PhoneBook/getAll')   // Your promise object
            .then(...)  // Instructing the promise object to call the function in the brackets once it completes successfully
            .fail(...);  // Instructing the promise object to call the function in the brackets if it fails
```

# .Catch
.catch is used for recieving errors when a promise is rejected, allowing us to do something after the error happens e.g log the error or retry the request. 

```js
axios.get('/api/PhoneBook/getAll')   // Your promise object
            .then(...)  // Instructing the promise object to call the function in the brackets once it completes successfully
            .catch(...);  // Instructing the promise object to call the function in the brackets if it fails
```

# Promise states

Resolve - the promise was resolved successfully

Reject - the promise was rejected

# Chaining promises

We can chain promises together, to have multiple results happen after a promise handler has been resolved. Chained promises are sequential so they happen one after another

```js
axios.get('https://maps.googleapis.com/maps/api/geocode/json?&address=' + this.props.p1)
  .then(response => {
  this.setState({ p1Location: response.data});
    return axios.get('https://maps.googleapis.com/maps/api/geocode/json?&address=' + this.props.p2);
  })
  .then(response => {this.setState({ p2Location: response.data
 });
    return axios.get('https://maps.googleapis.com/maps/api/geocode/json?&address=' + this.props.p3);
  })
  .then(response => {this.setState({ p3Location: response.data
 });
  }).catch(error => console.log(error.response));
  
  ```
  
 # Which order will this be executed in
 
 ```js
let trees;
fetch('
http://example.com/movies.json') //  
.then(response => response.json())  
.then(data => trees = data)
.catch(err => console.log(err));

Element.val(trees);
 ```

# Homework 

Go through the Udacity course on Promises 

https://classroom.udacity.com/courses/ud898

How to set up exoplanet explorer 

1. Open up git Bash and clone the repo using git clone https://github.com/udacity/exoplanet-explorer
2. Go to the folder using cd exoplanet-explorer and install gulp using npm install -g gulp bower
3. Install the polymer starter kit npm install && bower install -f polymer-starter-kit
4. Create a json file called npm-shrinkwrap.json and add the following line
Tutorial explaining npm-shrinkwrap.jspm : https://timonweb.com/javascript/how-to-fix-referenceerror-primordials-is-not-defined-error/

# Other resources

https://javascript.info/promise-basics

https://javascript.info/callbacks

https://javascript.info/promise-chaining
