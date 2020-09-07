# Basics of deployment

Don't be that person that walks around and ask people to check out your shiny webapp at http://localhost

Unfortunately, your website is not automatically reachable from the internet.

When you type a url into your browser, your browser will first check for a DNS record that is associated with the url.
It will then use the DNS record to resolve the url (e.g. www.google.com) into an IP address.
After running a bunch of procedures to make sure the server located at the IP address is safe,
your browser downloads the website content you've requested for and finally display it.


Although you could technically host your website from your computer, everyone uses some kind of host providers to save both time and effort.
They're cheap, reliable and generally very easy to use.
Learning and having a basic understandings on how to host a web app using solutions like GitHub and Heroku is incredible useful.


## **Static webapp** vs **Dynamic webapp**

Before we learn how to deploy your webapp, we need to learn which kind of webapp you have.

There are two types of web apps and they generally deploy differently with web hosting providers.
It is important to classify which webapp you have developed.

Answering this set of questionnaires might help you figure it out.

1. Does your webapp behave differently for every person?

2. Does your webapp build the website with server-sided code?

3. Does your JavaScript controls what gets displayed?

If you answered **yes** to question 1 to 3, you most likely have a ***dynamic webapp***.

If you answered **no** to the questions, you most likely have a ***static webapp***.

Although it takes more resources to host a dynamic webapp than a static webapp, as long as you don't have any server-sided code
you can still host them with a static web hosting provider.


## GitHub pages (static web hosting provider)

Getting your "Hello World" onto the internet is not a difficult or expensive task. One of the easiest way to set this up is with GitHub pages.
GitHub provides everyone with free static web hosting and one single domain name under "your-username.github.io".

- To host a static website under the GitHub domain:

[Publish and share your own website for free with GitHub](https://medium.com/@svinkle/publish-and-share-your-own-website-for-free-with-github-2eff049a1cb5)


- To host a React app under the GitHub domain:

[How to deploy your React app into Github Pages](https://blog.usejournal.com/how-to-deploy-your-react-app-into-github-pages-b2c96292b18e)


- Messing with DNS records can be confusing, but let's do it anyways:

[Linking A Custom Domain To Github Pages](https://richpauloo.github.io/2019-11-17-Linking-a-Custom-Domain-to-Github-Pages/)

## Heroku (static or dynamic web hosting provider)

Heroku is a platform for mostly targetted by developers to deploy dynamic webapps. It can host webapps running on Node, Ruby, Java, Scala, PHP and more.
It is generlaly more complicated than hosting static web apps on GitHub but being able to deploy your shiny webapp is worth it.

- Hosting a static website under Heroku with code on GitHub

[Hosting a static website on Heroku – The easy way](https://ashish.ch/hosting-a-static-website-on-heroku-the-easy-way/)


- Extensive tutorial on how to host a Node.js app on Heroku

[Getting Started on Heroku with Node.js](https://devcenter.heroku.com/articles/getting-started-with-nodejs)