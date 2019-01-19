---
title: IDEs are dead. Long Live Development Environments. (Part 2)
subtitle: "The benefits of stepping away from your IDE."
layout: post
categories: ["Tools"]
comments: true
---

If you haven't yet, you may want to refer to [part 1 of this series]({{ site.baseurl }}{% post_url 2019-01-05-step-away-from-your-ide %}) where I present a reasoned argument against using an IDE. Now let me try to explain why it was so beneficial for me.

I attribute major positive impacts to my professional competency as a developer to pulling away from my IDE and creating a development environment for myself. Below, I attempt categorize the positive impacts into 4 major groups.

### 1. Increased competency with individual tools

I first noticed that by using some tools directly, I began to understand them better than I did when I was using them through the abstraction of my IDE. Interacting with a tool on its terms (the interface that it provides) forces you to learn the concepts inherent with the tool rather than the way they have been abstracted away by your IDE.

For example,

- **Git**. Git's CLI is well known as being confusing and inconsistent. Many choose to use Git through their IDE of with applications like Tig, SourceTree, Kraken, etc... While these tools can be beneficial in specific use cases (I find no shame in relying on SourceTree or BitBucket for complicated diffs) they generally obfuscate the underlying concepts of Git. Learning to use Git's CLI has allowed me to extract more value from this notoriously complicated tool.
- **Dependency Management** (NPM, Yarn, Bundler, Gradle) Using the command line interface for these tools rather than the menus in an IDE forced me to better understand the role that they play in the software development lifecycle. When I was a pure IDE user, I knew that in some cases I had to run a *gradle refresh* or *gradle build* but these were actually more like debugging steps when something went wrong in my local environment. After learning the tools individually and directly I better understood when I needed to use them.

### 2. Improved debugging skills

I next noticed that when a production issue arose I had become much more comfortable with jumping on servers and getting to the bottom of an issue. When I was purely an IDE user, the thought of understanding how an application was running on in our target environment seemed much more foreign than the comfort of my Eclipse's GUI. Working primarily in a terminal and interacting with tools via their CLI led me to be much more comfortable with ops-related tasks. It also helped me come to understand the OS I was using more thoroughly.

### 3. Becoming a technical resource

After I noticed my increased ability with individual tools and improved debugging skills in my day to day software development activities, a third interesting benefit began to manifest — people began to come to me when they had problems with an individial tool. This may seem like an obvious progression as you read this blog post, but as it was happening to me, I was not planning to become 'the Git guy' when I started using Git directly via its CLI but nonetheless from time to time coworkers would come to me with a problem and much to my surprise I was often able to help them.

### 4. Adaptability

Finally, I noticed that when I switched development stacks, I was able to adapt easily to a new set of tools. Once I became somewhat 'intimate' with the tools in the first stack that I learned (Java based webapps) I then moved to a fullstack Javascript environment. I was a little nervous moving from Java to fullstack JS, but I found myself asking diagnostic questions based on tooling to get me through it. Rather than making a list of all the new tools I needed to learn to be a successful fullstack Javascript developer (and then researching them one by one), I was able to use the mental models I had of the tooling in my previous stack to gradually come to understand the new one. I would speak to myself like this:

> Alright, I need to pull down the dependencies for my project. In the past I used Gradle for that. What do I have now? NPM. Great. Let's see what the equivalent of `gradle build` is for NPM.

## In Sum

In the end I was often pleasantly surprised to find that from stack to stack, smart people have developed tools that share similar roles and very often these tools even use similar terminology. (Moving from Yarn to Bundler for example required very little research)

---

So, are you sold on the benefits of ditching your IDE yet? If so, come back soon for the last post in this series where I give the practical steps that I followed to step away from my IDE. In the meantime, let me know in the comments if you have found similar benefits.
