# Enhance Existing Project 

OpenClassrooms Front-End Developer path project: 'Enhance an existing project'. The project brief of this project can be found in the documents folder above. 

## Introduction
The first commit of this repo (see commit history) contains the code I was given to work with by Open Classrooms. The code is the code for a basic TodoList application, which  behaves like a Single Page Application. It uses Vanilla JS (ES5) with an MVC (Model – View – Controller) pattern, routes based on location hashes, a template, localStorage, and NPM packages for CSS and unit / functional tests. It’s a frontend application with no backend / database. 

## Technical documentation & competitor performance audit 
In the documents folder above you can find the technical documentation that I wrote for this project. It contains: 
* installation guide
* design and structure overview
* testing overview
* reference guide which was generated with documentation.js 
* my analysis of the performance of a competitor site 

## Bugs
Task: find and fix the 2 bugs. 
* Bug 1 turned out to be a simple typo (see commit history). 
* Bug 2 had the potential to cause a conflict between duplicate IDs. This had to do with the way IDs were generated (randomly generating a string of 6 numbers). Instead I used Date.now(), which is a safer solution for the way the app is set up at the moment (e.g. no database, which means todos are being saved in localStorage) since 1 user cannot possibly create more than 1 todo in the same millisecond. However, in a real-life situation you would most likely have a database with automatically incrementing ID numbers. 

I found 2 more bugs while testing:
* Bug 3: the toggleAll button (caret sign) doesn't work. The reason for this is that the button, which is under the hood an input field, does not have an ID, which means it wasn't linked to its label. And that link is necessary for the click-event to work. 
* Bug 4: console.error (404) stating that learn.json cannot be found. Apparently base.js line 248 in the node_modules is expecting to find a learn.js file inside the todomvc-common folder, which isn't there. Since base.js is not used by the app, I commented out its script in index.html for the time being. 

## Optimising loops
I have changed a couple of loops to make them faster or easier to read (or both). I have also realised that some things do not optimise loops, even though you can find the advice all over the Internet. They fall into the following categories:
* minimising property lookup --> was tested in jsperf and it turns out there is no difference in speed.
* initialising loop variables inside the loop instead of outside.
* .trim() instead of while loops to remove white space --> tested in jsperf and is a little slower, but easier to read.
* refactoring 2 for loops into 1 loop, because 1 was redundant. 
* replacing a for...in loop with Object.assign, which is faster. 
For each 'optimisation' see commit history.  

## Testing
To view all tests I added, either view commit history or go to test/controller.spec.js and look for the following comment: // TODO: write test. 

In the technical documentation (documents folder) I have briefly explained how I think the testing was set up. 
