---
layout: post
title: "The Serverless Sea Change"
subtitle: Serverless architecture might have a shot
categories: ["What I've Been Reading"]
comments: true
---

I read a great article at InfoQ this week called [*The Serverless Sea Change*](https://www.infoq.com/articles/serverless-sea-change). Generally, the argument made is that code leads to technical debt, therefore the solution with the least amount of code wins. For example:

> If you are building a Serviceful Serverless application, you will need to spend significantly more time on research than you would with an application where you will write everything. This is because you will be implementing much more functionality of the application on services, and you need to verify that you are selecting the correct service. You also need to figure out the right way to integrate the service with your application. So instead of spending an hour or two looking for packages you might leverage, you should think about spending days and even weeks writing proof-of-concept code and testing different options.
> 
> Another way to say this is in two equations:
> 
> 2 Weeks Research + 1 Day Development → N Lines of Code to Maintain
> 
> 1 Day Research + 2 Weeks Development → 10 ⋅ N Lines of Code to Maintain
> 
> On average, ten times more lines of code is ten times more technical debt, which means increasingly slower and less predictable future development velocity, and systems that cannot be well maintained by the average developer. 

I've generally remained skeptical as to whether the advantages of serverless architectures outweigh the benefits, or to put it another way, if there are any advantages when all is sasaid and done. For me, the looming issues are:

* Vendor Lock-in
* Conversely, the portability of any artifact targeting a FaaS platform
* The amount of glue needed to make serverless work (any AWS Lambda demo I've seen spends more time gluing AWS services together than it does writing code)
* In the case of AWS, many of the glue services are still beta products
* Ease of local development
* The *Cold Starts* problem

I remain skeptical, but this article does a great job of explaining and arguing for the benefits. Also, perhaps I am wrong (!) and we are a few years away from a true "Serverless Sea Change".

Be sure to check out the whole article over at [InfoQ](https://www.infoq.com/articles/serverless-sea-change).
