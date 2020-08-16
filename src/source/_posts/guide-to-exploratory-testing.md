---
title: A Guide to Exploratory Testing
seo_description: Learn about the benefits of Exploratory Testing and how to use it on your team.
promo_photo: /content/images/2020/casual-testing.jpg
date: 2020-08-16
tags:

---

_”Automated testing is king!”_

This is a sentiment echoed by software and QA engineers across industries. And it makes sense! Verifying a piece of software works as intended is best achieved by an automated process. But that’s not the only thing we should be testing.

Tests might tell us that something is working, **but they won’t tell us how it could function better for the people using it.** We like to delegate this problem to domain experts and designers. But what’s the equivalent of an integration test in the user experience design world?

Do we need another set of design experts for this? QA design engineers? Do we need to organize focus groups and interviews? What if we can’t afford any of this? What if you’re an offshore team that can’t get approval to talk to customers?

There’s a much simpler solution. One that’s on budget, sensible, **and driven by empathy towards people who will use the product.**

## What Is Exploratory Testing?

Most testing practices define a set of flows and validate their execution. They ask: _does this work the way we defined it?_ In contrast, with Exploratory testing, we want to see if those flows make sense and if there’s something we forgot to define. 

In 2018 I wrote _[“Output vs Outcome”](/2018/output-vs-outcome)_ which comes as parallel to that. Most of the testing we do verifies that our _outputs are correct._ **Exploratory testing attempts to confirm outcomes and inform future goals.**

The weight of practicing this does not fall on the engineers. Engineers or designers should manage the process, but they aren’t necessary practitioners who will carry it out. (But they are free to take part!)

### Who Should Test?

Everyone! Get as many people as possible invested in using the software you’re building and get them to ***think.*** Everyone in the organization should invest a few hours per month to do this. Sales, marketing, management, heck even your aunt and your favorite barista should chime in.

### What’s the Process Like?

<figure class="blog-post-image"><img src="/content/images/2020/exploratory-testing-diagram.png" alt="Diagram: text, learn, execute, repeat." /><figcaption>Test, learn, execute, repeat.</figcaption></figure>

There isn’t a strict process. *“Freestyle testing”* gets mentioned and this puts people off. The current trend is that every manager will insist on a well-known and proven process. 

Exploratory testing isn’t complete chaos, though. There should certainly be a pre-defined way we expect a tester to document and report their findings. But the way they will conduct the test itself is what’s left to the individual.

It’s a process that values individuality and diversity. The more diverse the testers, the more interesting the findings. Here are some of the types of diversity we’re thinking of here:

- **People use their devices in different ways.** For example, it’s be great to have both keyboard-heavy users and folks who avoid using (or cannot use) the keyboard as testers.
- **Unique experiences and backgrounds** lead to different expectations of how the business process the software is enabling is supposed to work.
- People from **different professions use different software** and they come with different expectations on how your software is supposed to function.

### Charters and Timeboxes

You don’t always have to test the whole system. Instead, you can set specific testing goals, commonly referred to as charters. An example might be: _“Explore the newest filtering options”_ or _“Explore the new report builder interface.”_

Some teams also like to timebox these tests. I’d say that makes sense if your testers already know the system a bit and are trying to only test one part of it. For a full system test, I would not assign any explicit timeboxing.

### Documenting the Test

**The testers should ideally record themselves while testing.** Screen + voice recordings are ideal, but making a voice recording is fine too.

The purpose isn’t necessarily so others could review (though that would be great!), but for the tester to refer to the recording while they create their documentation. This way they can easily grab screenshots or refer to a time segment where something weird happened. It also ensures that they don’t forget any details.

Writing things down as you’re testing is a burden that takes away from the exploratory nature of the process. You can do that later.

## Quantifying the Testing Data

A bit of a problem with this approach is quantifying the results and value that they bring. This depends on the data you get, so let’s look at what you can expect.

### Onboarding Issues

If a tester isn’t a domain expert or has never used the software previously, you could expect some of their problems and feedback to be related to the onboarding process. If this product is alien to them then this will be a good test of how easy it is for someone to pick up and use your software.

### Domain-related Issues

This is the **jackpot category.** If a domain export identifies something is wrong with how the system displays or performs a business process then you’re getting a lot of value of this testing practice.

### Bugs

Finding bugs before your customers do is extremely valuable and Exploratory testing will likely result in the discovery of some bugs. While this is great, don’t focus solely on the bugs, look for all the other issues as well!

### Usability Issues

The more diverse your testers, the more you can expect to learn about usability problems. Strive to include people with disabilities in your organization!

### User Experience Issues

Look for comments like _“that felt weird”_ or _“I wasn’t sure it actually did [the thing].”_ These will inform you of situations where your software isn’t clearly communicating that’s happening. Your software should solve problems, not create confusion.

## Using the Testing Data

Someone will have to crawl through the testing documents to identify all the different issues and formalize them into tasks. This is likely the domain of a QA lead, designer, or product owner. Obviously, it depends on the type of organization. At any rate, they **will spend a lot of time doing this** and they will get better at it as time goes on.

## Second-order Benefits

There’s some other benefits worth considering as this is a relaxed, team-orianted activity:

- Everyone learns more about the system and studies do show that people get more invested the more they are involved in something.
  - I’ve noticed that **salespeople especially benefit from understanding the system.** The more they know, the better they are at answering the questions of potential customers. The number of times they have to say _“I’ll get back to you on that”_ decreases and their confidence grows.
- It teaches people how to test and investigate better. That will improve productivity in future testing practices. 
  - It’s valuable for a junior QA tester to gain this sort of 360° experience with the system.
- It’s an organization-wide effort that brings different departments together. This improves cross-team communication and understanding.
- It helps inform future development. It’s better to crowd-source a lot of suggestions based on actual usage, not hypothetical assumptions.

<figure class="blog-post-image"><img src="/content/images/2020/who-should-test-software.png" alt="Diagram: Asks should you test? Are you a tester? No? Doesn’t matter you should still test!" /><figcaption>Show this diagram to your co-workers.</figcaption></figure>

## Get Going!

So, what are you waiting for? Get everyone together, share this concept with them and allow everyone an hour to sit down and explore. You’ll be amazed by all the different discoveries and perspectives!
