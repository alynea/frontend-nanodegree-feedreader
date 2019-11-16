# Project Overview
This is a project to test a feedReader code in Jasmine.js with jQuery to select DOM elements. 

The project uses Jasmine to write a number of tests against the RSS feed application.These will test the underlying business logic of the application as well as the event handling and DOM manipulation.


# How to run the app locally
## Quick start
A simple way to go is to clone or download this git repository to your local machine. Locate to the repository folder and  open `index.html`, you should be able to see the feeds load. 

## Run the app on a server
1. clone this repository to your project folder
2. ensure you've installed node.js. For more details, please refer to [node.js official website](https://nodejs.org/en/)

## Tests in Project
### Test Suite "The Menu"
By default, the body should be with class menu-hidden. 
By using jQuery to select the BODY element and check to see if it has 'menu-hidden using the `has class`. So that the test should detect if the `body` tag contains 'menu-hidden'.

By using JQuery `trigger` on The click() event is used to check if the 'menu-hidden' class exists to ensure the function goes well.  

### Test Suite "Initial Entries"
In `app.js`, it runs loadFeed() to load the data from each feed. If the feed load successfully, it will render the HTML inside the feed container `DIV.feed`. 
Since `.entry-link` is an rendered element when feed successfully initialised, by checking if the .feed HTML after loading can see if the entries has been loaded properly. 
The loadFeed() is asynchronous so that the test should run beforeEach() and done() to ensure the loadFeed() runs in the test. 

### Test Suite "New Feed Selection"
There are more than one feed in the allFeeds. The loadFeed() function load specified feed with the id(index).
The second feed content should be different from the first feed. So that by comparing the rendered HTML content, we can check if the program loads a different feed with the function instead the same one. 
The HTML can be get in jQuery .html() function. 