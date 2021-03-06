# Enhance an existing project

In the professional world, you'll often be working on an existing codebase. What to do when you find yourself with someone else's code as part of your own job duties? How can you improve it? 

Taking over projects seamlessly and quickly is a skill that will come in handy!

Executing a project from start to finish is "easy" (well, relatively speaking). You end up with intimate knowledge of the project and all its quirks. However, it can be much more difficult to take over someone else's work, especially when there are no existing tests — but there are existing bugs.

Here's the scenario. You just joined a small team that believes all of the world's problems are due to people being disorganized, and that more focus would solve everything. That's why they've built what they claim to be the world's best to-do app. Maybe the app itself is cool, but the code behind it is a total mess! They've brought you in to add tests to the codebase and to fix a couple lingering bugs.

In order to improve the project, you'll first need to download the project code: 

[Download project](https://s3-eu-west-1.amazonaws.com/static.oc-static.com/prod/courses/files/project-8-frontend/todo-list-project.zip)

Check out how it's structured, and try to understand how it works. You'll be fixing bugs, adding tests, and optimizing performance.

## Step 1: Fix the bugs
There are 2 bugs in the code, and it's your job to find them! Here are some hints:
* One bug is a simple typo.
* One bug involves an introduction of potential conflict between duplicate IDs.

One of the bugs is severe enough that to-do items can't even be added!

You'll need to go hunting in the code for these bugs like they're Waldo! Once you find them, you'll fix them because they're preventing the code from functioning properly.

There are also some improvements in the code that can be made that aren't necessarily bugs. Try to find where loops can be optimized and if there are any logging statements that may not be necessary.

## Step 2: Add tests
As mentioned above, you might notice that this project has some tests but definitely not enough. To take over the project, the first step should be to add as many tests as you can. The goal is to create a real test foundation to support the project. That way, when you change it later, you can rely on these tests to make sure that you don't break anything.

This step may appear to be a bit long and tedious, but it'll save you time and bad surprises later.
You'll need to run `npm install`  on the project in order to install the requisite Jasmine materials.

There's an existing test file called `ControllerSpec.js`  in the project, and you should find all instances of the comment below and add tests there.

// TODO: write test

Hint: Save yourself time and get the job done more quickly by adopting a TDD approach. Like all the top developers, if you write tests and fix bugs simultaneously, you can use the tests to identify what’s broken, which makes the bug fixing faster.

## Step 3: Analyze performance
The owners of the project have asked you to analyze the performance of a competitor site in order to identify what works well and what doesn't, if someday you decide to scale the app. Here's the [competitor site](http://todolistme.net/).

Use your browser's developer tools to analyze this website's performance. Pay attention to the resources used by certain elements of the site, what's slow vs. what's not, etc. You should pay attention to the resources used by advertisements on the site and to the resources used to perform to-do functionalities in the list itself.

You'll then write an audit performance document that consists of some written text about the competitor's performance, how it differs from your own app, and how to optimize performance when scaling your own app up someday. This should be approximately 300-500 words long and as quantitative as possible.

## Step 4: Write technical documentation
Now that you know the codebase by heart, take your audit document and add some more information to it. It's time to write technical documentation! 

Simply put, you'll need to write documentation that describes the project, how it works (technically), and include your audit writeup in the documentation. You can do this in any format you want, whether it's a wiki on Github, a text document, or something else.

## Presentation
You'll do an oral presentation of your project with an assessor in order to simulate real-life conditions.

## Skills
*	Take over an existing JavaScript project
*	Optimize the performance of a project using DevTools
*	Implement unit and functional tests in a web application
