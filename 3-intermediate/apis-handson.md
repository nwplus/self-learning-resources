## Getting more hands-on with APIs

### Calling / Using an API

When do I need to do this?

- You need to request information to some external service (e.g. getting the current weather, fetching your facebook posts, etc.)
- You need to communicate with a service someone else built (e.g. your teammate)

This is usually done through the aforementioned HTTP requests. Each language has a different way of making these requests. 

#### Python

`requests` library → [https://requests.readthedocs.io/en/master/](https://requests.readthedocs.io/en/master/)

This library makes it dead simple to make HTTP requests. If you have Python installed already, you can get this library by typing

```bash
pip install requests
```

You can then use `requests` in Python by importing it. 

```python
import requests

# make a GET request to the GitHub API and store
# the result in the variable r
r = requests.get('https://api.github.com/repos/psf/requests')

# r.status_code will tell you the status of the request
print(r.status_code) 
# should print out '200'

# you can then convert the actual body of the response into
# a python readable form (a dictionary in this case)
body = r.json()

# then you can get certain fields from the body
print(body["description"]) 
# should print out 'A simple, yet elegant HTTP library.'
```

#### JavaScript
`XMLHttpRequest` → This is a built-in JavaScript object that lets you make HTTP requests in Vanilla JavaScript! Example usage is as follows,

```jsx
// create a function that tells JavaScript what to do
// after receiving a response from the server
function handleResponse () {
    // create a 'response' variable that contains the response data
    const response = this

    // print out the status of the request
    console.log(response.status)

    // get the body of the request and parse into JSON 
    // (allows JavaScript to easily manipulate the data)
    const body = JSON.parse(response.responseText)
    
    // print out the description field again
    console.log(body.description)
}

// create a new request object with the name 'r'
const r = new XMLHttpRequest();

// add an event listener so that we run 'handleResponse()' after the
// request 'r' loads
r.addEventListener("load", handleResponse);

// make the actual request to the resource using GET
r.open("GET", "https://api.github.com/repos/psf/requests");
r.send();
```

You can learn more about `XMLHttpRequest` here: [https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest)

`Axios` → Axios is a Promise-based alternative to XMLHttpRequest that works in Node.js too :)) I'm not going to go into too much detail but it is definitely a more clean and easier way to do HTTP requests in JavaScript if you don't mind using external libraries. You can read more here: [https://github.com/axios/axios](https://github.com/axios/axios)

You can read a more detailed guide here: [https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Client-side_web_APIs/Introducti](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Client-side_web_APIs/Introduction)

##  Building your own API

When do I need to do this? → 

- You need to serve up some information (e.g. get user details from a database)
- You need to cobble together a bunch of other APIs (e.g. get data from current weather and feed it into Google Search API)

The implementation vastly differs per language, but the main concept is the same: you create a HTTP server that listens for and responds to requests from the internet. Both Python and JavaScript have frameworks that make it simple to do just that. Going into the implementation of each is a little outside the scope of this guide, so instead we'll link a few good guides and tutorials that we've found to get you started.

### Python — `Flask` framework
Site → [https://flask.palletsprojects.com/en/1.1.x/](https://flask.palletsprojects.com/en/1.1.x/)

**Resources**

Installation → [https://flask.palletsprojects.com/en/1.1.x/installation/](https://flask.palletsprojects.com/en/1.1.x/installation/)

A 'hello world' → [https://flask.palletsprojects.com/en/1.1.x/tutorial/layout/](https://flask.palletsprojects.com/en/1.1.x/tutorial/layout/)

A full Flask API by example → [https://realpython.com/flask-by-example-part-1-project-setup/](https://realpython.com/flask-by-example-part-1-project-setup/)

LHD Flask Example → [https://github.com/jackyzha0/lhd-build-python-webapp](https://github.com/jackyzha0/lhd-build-python-webapp)
</details>

### JavaScript — `Express` framework

Site → [https://expressjs.com/](https://expressjs.com/)

**Resources**

Installation → [https://expressjs.com/en/starter/installing.html](https://expressjs.com/en/starter/installing.html)

A 'hello world' → [https://expressjs.com/en/starter/hello-world.html](https://expressjs.com/en/starter/hello-world.html)

A complete guide → [https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs)

## More advanced topics

### API Keys

From Wikipedia:

> An application programming interface key (API key) is a unique identifier used to authenticate a user, developer, or calling program to an API

When you start looking at third-party APIs, many of them will mention API Keys. Basically, these are long strings that tell the API who you are so they know you have permission to access it. You can find more information on how to include the API key here: [https://en.wikipedia.org/wiki/Application_programming_interface_key](https://en.wikipedia.org/wiki/Application_programming_interface_key)

### Hosting your API

What do you do after you've made an API? You may have noticed that your API only lives on your local machine and that nobody else can use it! So, how do we expose our API to the internet? The easiest way to do this is to host our API on a third-party provider. Just to name a few, [Heroku](https://www.heroku.com/), Google Cloud (GCP), and Amazon Web Services (AWS) are all widely used. Below, we've provided some resources and starter guides for each of these to help you get your API onto the internet!

[https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs/deployment](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs/deployment)