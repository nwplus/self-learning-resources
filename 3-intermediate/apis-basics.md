## What the heck is an API?

Think of it as the language that two programs can use to talk to and make requests to one another.

> "In other words, an API is the messenger that delivers your request to the provider that you’re requesting it from and then delivers the response back to you."

In fact, the entire web *runs* on APIs! Every time you visit a webpage, you're requesting information from a server and doing something with it. To make a post on Facebook, you make a request to Facebook's servers.

## The basics

What is a 'request' → a request for the server to perform some action on a resource. This can be retrieving user information, updating some data, etc. 

The defacto way of communicating on the web is usually Hypertext Transfer Protocol (HTTP). It's also why you see `http://` or `https://` in the URL of most websites. This protocol also defines a bunch of different types of requests that you can send! The two most common ones we will cover in this guide are the GET and POST methods. 

GET → retrieves specific data. (e.g. Load this webpage)

POST → sending data to a server (e.g. submitting a form)

You can find more about the others methods in some of the resources below.

- [https://www.tutorialspoint.com/http/http_methods.htm](https://www.tutorialspoint.com/http/http_methods.htm)
- [https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods)

Now, after you make a request, the server (if it's alive) should return you a response! The response should include a **status code** that tells you about the type of response you got. A common one that you might see is the 404, which tells you that the server couldn't find the thing you were asking for. Here are a few other pretty common categories:

- 2xx → successful
- 4xx → bad request
- 5xx → server error

If you'd like some more detailed information on these status codes, this is a good resource: [https://www.restapitutorial.com/httpstatuscodes.html](https://www.restapitutorial.com/httpstatuscodes.html)

### How/when to use them in a project

Great, so now that I know a little bit about how these APIs kind of work, how do I use them in my projects?