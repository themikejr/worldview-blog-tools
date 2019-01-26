---
title: The One-Hand Approach to Production Support
subtitle: Preserve developer focus, nurture developer autonomy
layout: post
categories: ["Teams"]
Keywords: production support, software development teams, antifragility
comments: true
---
Across the industry, as the teams trend away from being project-focused toward being product-focused, an increasing number of software developers find themselves being responsible for 'support duties'. These responsibilities may include answering user questions, attempting to recreate reported bugs, and trying to recover from a system outage in production. There are reasons why it is good (this is the spirit of *DevOps* in my opinion) that developers will increasingly participate in these duties, but for teams that are taking these responsibilities on for the first time, confusion abounds.

## Assumptions

- Production incidents *will* happen
- It is in the best interest of the team and product for developers to become skilled at handing production incidents
- We should aspire to [Antifragility](https://en.wikipedia.org/wiki/Antifragility) in our systems, our teams, and as individuals.

## The All-Hands by Default Approach

To my surprise I have seen managers and developers who prefer an unorganized, all-hands approach to production support. Typically, a scenario will play out like this:

1. Production incident is reported to some sort of channel that is 'public' to all developers
2. Since there is not a dedicated person to handle all issues for this given time frame, a manager type will soon be contacting developers to find out who is working on the issue.
3. Meanwhile, a developer notices the problem and immediately notifies his/her peers
4. Physical or virtual huddle happens and 'all hands' are on deck for fixing the issue
5. Typically developers that have more experience with the system (or perhaps have more mature skill sets) lead the troubleshooting until a solution is found

I suppose developers and managers might prefer this approach for the following reasons:

- Having a huddle creates an atmosphere or appearance of productivity and progress
- When all developers are in the huddle, each can suggest solutions or hypotheses that are unique to their skillset and experience (seemingly shortening the time that it takes to solve the problem)
- From a developer's point of view, this approach may provide more *psychological safety* since they aren't the only one working on an issue

## Problems of the All-Hands Approach

There are hidden costs to the all-hands approach.

First, it may seem like having a support incident channel that is public to all developers is a good idea, but I think what most managers don't realize is the amount of distraction that channels such as these create. If a developer is told that part of their job responsibility is to monitor logged incidents, their concentration is going to be almost [permanently compromised](http://calnewport.com/blog/2016/09/06/a-productivity-lesson-from-a-classic-arcade-game/) to some degree. One extreme example I recently heard was a developer, who faced with the responsibilities of supporting an application, opened up the application logs *every morning* and had them visible on her screen for the entire day. If something went wrong with the application, she claimed to be able to detect a change in the shape of the text that was flowing on the screen. Imagine if this person's manager understood that this person was compromising their concentration nearly 100% of the time to visually monitor application logs!

Less extreme situations still are quite a drain on a developer's ability to focus. If you are not convinced of this I suggest taking a look at [Deep Work](http://calnewport.com/books/deep-work/) by Cal Newport (decent summary [here](https://fastertomaster.com/deep-work-by-cal-newport/)).

In addition to a near constant compromising of developer focus, consider the sheer *cost* of involving everyone on the team in each production incident. As I mentioned in point number five of the *All Hands* approach, it has often been my observation that despite all hands being present, a single developer usually ends up leading the charge at finding a solution and applying it. Given this, it is especially egregious to think that all of the members are pulled into a huddle for the incident when a subset of them will actually be contributing meaningfully to the solution.

## The One-Hand (by Default) Approach

What if I could suggest an approach to handling production support that decreased distraction to the team and fostered improvement of skills and self-confidence for individual developers? That's exactly what the *One-Hand* approach is. It goes something like this:

1. Notifications of production incidents are fed to a developer who is 'on call' for the given time period (let's say they are on call for the current week). Developers who are not on call are expected to continue with their normal work.
2. The developer works with the user (and outside teams if necessary) to resolve the issue.
3. The on-call developer knows that as a case of last-resort, they can involve their mentor (a developer peer) or lead to get the issue resolved.

With such an approach you decrease developer distraction and increase individual problem solving skills over time.

There are some cultural presuppositions that need to be installed for this to work properly. Primarily, the developer on call needs to see a production incident as an individually assigned challenge — from which they can learn and be gratified for solving. Additionally, the developer on call needs to understand that they are providing value as they protect the team from distraction, meanwhile the team as a whole needs to cherish distraction-free focus time (aka "Deep Work") as a means to applying their unique skillsets so that they can deliver value.

Finally, the decision to bring another developer into a huddle needs to be understood as something undesirable but potentially necessary in a given instance. The developer on-call should set out thinking of pulling someone else in as a last resort, but the rest of the team should not think of this as an *ostrasizable* offense. If the team is mature enough to work under these assumptions, the One-Hand approach yields the following benefits:

- Protects the majority of the team from distraction
- Removes the latent stress of the entire team watching a public channel, waiting for something bad to happen
- Forces all team members to 'level up' the various skills needed for production support
- Each developer who handles an incident will have increased confidence and know-how
- Over time you decrease the amount of single-person dependencies the team has

This approach goes hand-in-hand with the idea of Antifragility. A team needs to be strengthened by various stressors in its environment. A system needs 'adaptive fault tolerance' (See the [Antifragile Software Manifesto](https://www.sciencedirect.com/science/article/pii/S1877050916302290)). An individual needs to be tested and strengthened to a degree in order to become better (interestingly, Jonathan Haidt even [applies Antifragility](https://www.youtube.com/watch?v=tvb7R6GF6CU) to childhood development).

## In Sum

Yes, there might be some situations where the All-Hands approach is needed. If these instances are not rare on your team, something else is probably gravely wrong.

Yes, the lead of the team or mentor will still be generally distracted as junior developers come to them with production incidents. This is the sad, lonely road  walked by the developer who chooses to mentor or take the lead on a team.

Ultimately, the One-hand (by default) approach ends up delivering a more focused and capable team and a generally saner work environment.

---

Do you violently disagree me? Do you have a legendary story from that night you were on-call? Let me know in the comments.
