# Basics of deployment

Don't be that person that walks around and ask people to check out your shiny web app at http://localhost

Unfortunately, your website is not automatically reachable from the internet.

## How do other websites get reached from the internet then? (Optional)
When you type a URL into your browser's address bar, your browser will first check for a DNS record that is associated with the URL.
It will first search locally in the cache then on the internet from various Domain Name System resolution services.
It will then use the DNS record to resolve the URL into an IP address that you can make requests to (e.g. www.google.com -> 23.245.12.211) .
After running a bunch of networking procedures to make sure the server located at the IP address is safe,
your browser downloads the website content you've requested and finally displays it.


Although you could technically host a website from your computer, everyone uses web hosting providers to save both time and effort.
They're cheap, reliable, and generally very easy to use.
Learning and having a basic understanding of how to host a web app using solutions like GitHub and Heroku is incredibly useful.

## **Static webapp** vs **Dynamic webapp**

Before we learn how to deploy your web app, we need to first learn what kind of web app you have.

There are two types of web apps and they generally deploy differently.
It is important to classify which web app you have developed so you can pick the right service to use.

Answering this set of questionnaires might help you figure it out.

1. Does your web app show different data for every person?

2. Does your JavaScript control what gets rendered?

If you answered **yes** to any of the questions above, you most likely have a ***dynamic webapp***.

If you answered **no** to all of the questions, you most likely have a ***static webapp***.

It takes more resources to host a dynamic web app than a static web app since it becomes more than just hosting a static file on the internet.
However, you can still host them with a static web hosting provider as long as your app is not a running server.


## Web hosting providers

### GitHub pages

*Note: GitHub pages is only for hosting static webapps*

Getting your "Hello World" onto the internet is not a difficult or expensive task. One of the easiest ways to set this up is with GitHub pages.
GitHub provides everyone with unlimited free static web hosting with one single domain name under "your-username.github.io".

**To host a static website under the GitHub domain:**

[Publish and share your website for free with GitHub](https://medium.com/@svinkle/publish-and-share-your-own-website-for-free-with-github-2eff049a1cb5)


**To host a dynamic React app under the GitHub domain:**

[How to deploy your React app into Github Pages](https://blog.usejournal.com/how-to-deploy-your-react-app-into-github-pages-b2c96292b18e)


**Messing with custom domains can be confusing, but let's do it anyway:**

[Linking A Custom Domain To Github Pages](https://richpauloo.github.io/2019-11-17-Linking-a-Custom-Domain-to-Github-Pages/)

### Heroku

*Note: Heroku is used to host both static and dynamic webapps*


Heroku is a platform mostly targetted by developers to deploy dynamic web apps. It can host web apps running on Node, Ruby, Java, Scala, PHP, and more.
It is more complicated than hosting static web apps on GitHub but being able to deploy your brand new dynamic web app is worth it.

**Extensive tutorial on how to host a Node.js app on Heroku:**

[Getting Started on Heroku with Node.js](https://devcenter.heroku.com/articles/getting-started-with-nodejs)


**Hosting a static website under Heroku with code on GitHub:**

[Hosting a static website on Heroku – The easy way](https://ashish.ch/hosting-a-static-website-on-heroku-the-easy-way/)

