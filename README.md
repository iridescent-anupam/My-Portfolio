# My-Portfolio
Portfolio created through Crio : https://anupamsanidhyacrio.netlify.app/

###Components/Frameworks used -###

* HTML (Frontend) - HTML is the standard language used to create webpage content.

* CSS (Frontend) - CSS describes how HTML elements should be displayed on the page.

* JavaScript (Frontend) - JavaScript is a programming language which can do data manipulation and update the HTML and CSS of a page.

* React (Frontend) - React is a JavaScript library for building user interfaces or UI components. In place of the traditional way to build interfaces (using HTML, CSS, vanilla JS), React provides utilities such as components and their states and also the usage of JSX to include HTML in the JavaScript code. This declarative way paves the path for creating painless interactive UIs.

* Gatsby (Frontend) - Gatsby is a React based framework to generate static websites which are fast. It provides a wide range of plugins, templates, and has performance, scalability, and security included by default. The plugins can range from the ability to pull in data from any kind of source (APIs, databases, CMSs) to even providing image optimization for faster loading of the website. Under the hood, Gatsby ends up using Node as the runtime environment for the JavaScript code.

* Netlify (Frontend) - Netlify is a service that we’ll use to deploy our Frontend publicly.

* NodeJS (Backend) - Node.js is a JavaScript runtime environment which can be used to run our Backend server. Note that it can also be used to run our Frontend as well, but here we’ll use it to run the Backend only.

* Express (Backend) - Express is a Node.js web application framework that provides a robust set of features for web and mobile applications.

* npm - node package manager is a package manager for Node.js packages, or modules

* Heroku (Backend) - Heroku is a service we’ll use to deploy our Backend publicly

* REST API (Interface between Frontend and Backend) - It is a standard request/response format that allows two components or applications to talk to each other.

![Overview](./Qprofile.png?raw=true "Overview")

We have used Heroku to deploy our backend (using node) here. However, we can use it to deploy our frontend too (gatsby + node runtime).

Once deployed to Heroku, they are served by popular web servers such as Apache, Nginx, etc.

But the key thing is, we don’t serve our frontend like a traditional web server, where a server would be listening on a particular port and code would be executed dynamically to first build and then serve content to the client.

Instead, we build the whole Gatsby + React code to generate static HTML, CSS, JS files. These files are served like the following - a simple server runs and the only (small) logic overhead it has is to decide which file(s) to send to the client. This makes it much faster to fetch the required files and render them.

An advanced version of the method mentioned above is widely used by CDNs (Content Delivery Networks), who also bring caching of assets, guaranteed availability, speed, etc. to the table.

Heroku has addons for CDN, however Netlify has everything required built in by default - as a product, they solely focus on serving static websites the best way possible, and are much widely used for these purposes. That is why we’ve chosen netlify for our frontend.