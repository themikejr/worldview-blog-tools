---
title: IDEs are dead. Long Live Development Environments. (Part 1)
subtitle: "Why you should step away from your IDE."
layout: post
categories: ["Tools"]
comments: true
---

## Preface

Generally, I don’t think there are one-size-fits-all solutions in software development and engineering. I’m going to argue that it will be good for you to step away from your IDE because it was good for me to do so. If you totally disagree with me, that’s cool! Tell me your experience in the comments section.

## The Sacrifice You Didn’t Know You Were Making

When it comes to being productive as a software developer there are many categories of personality that manifest regarding productivity. I speak from experience here, I’ve dabbled in nearly all of these. There are coffee addicts, nootropic pill-poppers, noise-cancelling headphone donners, binaural beat dweebs, flow-state seekers, text-editor worshippers, point-and-click mouse nuts, keyboard-only wingdings, the list goes on. I would like to take this moment to introduce what I consider a dangerous software developer personality, *the IDE indentured servant*.

The IDE indentured servant is the person who relies on their trusty IDE as a prized productivity tool but doesn’t realize that it’s actually holding them back. Whatever gains they may have gotten in short-term productivity (which I believe is a *false* productivity), they completely sacrifice when it comes to long-term productivity.

I’m here to tell you today that *IDEs are a drain on your productivity*.

**Use an IDE if you want to stunt your software developer development.**

**Use an IDE if you want to be a *lesser* developer.**

Do I have your attention? Cool.

Let’s go back to productivity for a second. Everyone knows a developer who’s measure of productivity is getting a feature deployed to a test environment so that they can start the next feature. These are the people who feel good about getting something ‘done’. These are also the people who usually forget to finish things in my experience. I have trouble with this myself actually. The gratification I get from ‘finishing’ something can lead me to prematurely move onto something else if I’m not careful. Let’s call this *short term productivity*.

Conversely we have *long term productivity*; finishing things that provide value and getting them right.

> Slow is smooth and smooth is fast.

> Measure twice and cut once.

There is truth to these aphorisms! (not least because Phil Dunphy champions the former). It’s the developer who desires long term productivity that needs to ditch her IDE.

## Why the IDE hate?

Think about what an IDE actually does. The most charitable description would be that it ties together many tools and utilizes them to give instant feedback to the developer. This actually might be true, but there is one terrible side effect that most don’t consider: IDEs abstract the developer away from the very tools that they are using. This abstraction generates a distance between the developer and their tools. This distance may be helpful in the short term (imagine training wheels on a bike) but will only hurt in the long term (try riding your bike off road being dependent on training wheels).

Don’t believe me?

Consider this for a moment: *becoming competently productive with a particular IDE is orthogonal to being competently productive in a given language technology stack*.

Learning how to use an IDE doesn’t actually teach you how to use the underlying tools that it ‘integrates’. Please join me in a short though experiment.

### The Junior Developer + Git

Take version control for example. Imagine a junior developer who joins a team and begins their first project, which happens to be written in Ruby. For the sake of the experiment, imagine that they know nothing about Git. They reach for the RubyMine IDE from JetBrains. RubyMine has a fair amount of VCS tooling off the shelf that helps you do things with Git. There is some overlap between the terminology used by RubyMine’s VCS features and the Git CLI, but it’s not 100%.

So the junior dev works on this project for 6 months.  They’ve been using the RubyMine VCS tools to commit and push their changes. At the end of 6 months, how much have they learned about Git?

I think we all know the answer. They have learned *very little* about Git. They have probably memorized the menu items or keyboard shortcuts that are needed to commit and push to a branch, but they probably aren’t aware of the differences between the Git index, staged files, and committed files for example.

I’m not saying it’s logically necessary for a developer to know the internals of Git to be successful. Being a software developer is about providing value to the people that we are making the software for. You don’t have to be a Git ninja to provide value. However, There will be a point though when the developer who doesn’t know Git very well will likely lose some of their work, blow away a remote branch accidentally, or get very confused when someone asks them to “Cherry pick” a commit. In this moment who is the person that every one turns to? It’s the guy who always uses the Git CLI.


### Some Personal Experience

My first project was in Java and we used CVS (shudder) for version control. I used the CVS tooling built into Eclipse every time I pushed, pulled, compared, etc… just like the rest of my team. There was one time where something went horribly wrong with the CVS repo on our CVS server. You know who my team needed help from to get it fixed? The token Emacs user that sat near us. He had been using the CVS CLI all along. He made quick work of the problem that we had. It was trivial enough for him to fix  that none of us ever understood what the problem was.

I humbly suggest that this will happen not only with VCS tools but dependency management tools, interpreters, compilers, application servers, linters, code coverage tools, and build tooling.


## In Sum

*In order to integrate developer tools into a single environment, IDEs abstract tooling away which has the unfortunate side effect of obscuring the developer from their tooling*.

It is my contention that this may be good for short-term productivity, but is almost certainly bad for long-term productivity.

Come back soon to check out the next part in this series where I explain why building my own development environment was so beneficial for me.

---

Do you completely disagree with me? Excellent! Please let me know in the comments. Otherwise, stay tuned for Part 2 of this series: *The Benefits of Building Your Own IDE*.
