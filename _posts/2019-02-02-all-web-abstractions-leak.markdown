---
layout: post
title: "All Web Abstractions Leak"
subtitle: Leaky abstractions make men old and grumpy
categories: ["What I've Been Reading"]
comments: true
---

[Gary Bernhardt](https://twitter.com/garybernhardt) had a great thread on twitter recently.

> There's no such thing as abstraction in web tools and never has been. Every framework claims that it will hide the complexity from you, but it always leaks through. You end up having to understand the framework, its dependencies, and the web primitives they're built on.

When I first joined a software development team, I remember having my mind *blown* as someone on the team walked me through the layers that made up the application. It was a SpringMVC web app that consisted of a view described the user interface, a model that held the data to be plugged into the view, and a controller that tied the model and view together and served requests. Hibernate was also involved in retrieving the data that populated the model. It was like staring under the hood of a car for the first time, seeing how carefully chosen components worked together to create this thing called a 'web app'. All of those layers! Not to mentioned future joys I would experience like debugging an ORM, tuning a database, becoming fluent in the unspeakable incomprehensibilites of WebSphere, learning languages that compile into other languages, and all of the other things I've buried in my subconscious. Early on though it was fascinating to see those layers and exciting to think I was going to be able to contribute to the creation of an application *that someone would be using* in real life.

Now days though, when I consider all of the things someone might have to learn in order to be a productive web developer, it really is daunting. The markup languages, stylesheets, a javascript framework, a language that compiled to JS, a build tool and dependency management, all just for the client side of the application. Imagining a world where the web (good luck well-defining that btw) is as abstracted to a developer and my operating system is to me... well it seems to good to be true.

The thread as some great examples and comments from others. [Read it unrolled](https://threadreaderapp.com/thread/1088523317089169408.html) on ThreadReader.
