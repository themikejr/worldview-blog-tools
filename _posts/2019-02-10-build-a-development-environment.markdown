---
layout: post
title: IDEs are dead. Long Live Development Environments. (Part 3)
subtitle: "Five steps to getting away from your IDE, mastering your tools, and building your own development environment."
layout: post
categories: ["Tools"]
comments: true
---
I've already written about [why you should step away from your IDE]({{ site.baseurl }}{% post_url 2019-01-05-step-away-from-your-ide %}) and [how I've benefited from doing so]({{ site.baseurl }}{% post_url 2019-01-12-benefits-of-stepping-away-from-your-ide %}). Now let's take a look at how this can be accomplished. As always these steps are based on my experience as a finite human being and thus your mileage may vary. The five steps are:

## 1. Begin using a single tool directly, outside of your IDE.

The first step is begin interacting directly with one of the tools that your IDE abstracts.
Choose a tool, and make it a goal to only use it directly (rather than from inside of your IDE) from now on.
Use the interface that that the tool defaults to. For example, if you choose to use Git directly, use the command line interface rather than another third party client.
If nothing else you will gain the advantage of learning a particular tools in more depth. Some ideas for which tool to pick:

- Dependency Management
- Build System
- Version Control
- Test Execution / Coverage
- Code Quality / Linting Tools
- Application Servers

## 2. Use all tools directly. Eventually only rely on the text editor in your IDE.

Repeat step one until you can use all or most of your development tools directly rather than through your IDE. The goal here is for the IDE to basically just become a text editor. At this point your development experience might feel slower than it was before, but what you lose in daily productivity will be rewarded in the long run with a better knowledge and command of your tools.

This isn't the place that you want to be long term, so work to get a good understanding of your tools quickly so that you can move onto steps 3 and 4.

## 3. Switch text editors.

Once you reach step two, you will most likely realize that your IDE is not a great text editor. It's big, slow, and is most likely lacking advanced features that specialized text editors have. Now that you only really have your IDE because you need a text editor, it's time to find a *your* text editor. Finding the right text editor could be a blog series of its own, but here are a few things to think about.

Finding *your* text editor is what some will call a journey. Ideally you want something that has:

- cross platform support
- large online community
- customization capabilities
- staying power

Text editors that have these qualities will like have a larger learning curve, but that's ok! You spend hours of your life editing text *every day*. Why not dig in and get good at it? I'm not the first one to say this:

> Use a Single Editor Well
>
> The editor should be an extension of your hand; make sure your editor is configurable, extensible, and programmable.
>
> (From *The Pragmatic Programmer)*

## 4. Slowly bring IDE functionality into your text editor.

This step always in progress for most developers. Once you are on the path to mastering your text editor, you will find it beneficial to begin adding little shortcuts to your editor to increase your productivity. For example, rather than switching to new terminal window to run your unit tests, write a macro (or something equivalent for your editor... perhaps a plugin?) that runs all tests in the visible file based upon a keystroke of your choice. Some ideas to enhance productivity in your editor:

- A fuzzy finder for file contents or names
- Ability to see the VCS history for a given file
- A shortcut to automatically format markup (chunks of XML, JSON, etc...)

At this point I anticipate some objections. Why leave your IDE if the goal is just to rebuild it eventually?
 There are two main reasons why bringing functionality back into your text editor is not just an insane re-doing of what you already had with your IDE.

First, recognize that by this point you have gained an enhanced knowledge of all the tools in your toolkit and become a text editing wizard. Any shortcut you add back is added from a position of knowledge (of your tools) rather than dependence (on your IDE).

Second, with this approach you only bring what modifications you need. You will end up with something much lighter than an IDE overall.

## 5. Build your environment.

Now that you are living and working with a set of development tools that you have glued together through your expert knowledge and experience, you can take it one step farther by noticing patterns in your daily development activities and automating those. For example, if you find yourself opening the same three terminal emulator tabs (and starting various tools in them) write a script that does that!

- Terminal Emulator: Customized Windows, Tabs, and Panes
- A Tiling Window Manager: i3, xmonad, kwm, Amethyst
- Window Manager with the Terminal: Tmux, Tmuxinator, Screen
- Make your environment portable: Store your configurations on GitHub or create a docker image that houses all of your tools and their dependencies

---

This is how I broke my dependence on an IDE. Have you? Let's hear how you did it in the comments.
