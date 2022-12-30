---
title: "Revisited: Avoiding Booleans When Designing React Components"
seo_description: I’ll clear out 3 misconceptions and provide another big benefit of sticking to the advice outlined in the original article.
promo_photo: /content/images/2020/designing-react-components-booleans.jpg
date: 2020-01-18
tags:
---

Last year I wrote a post titled <a href="https://spicefactory.co/blog/2019/03/26/how-to-avoid-the-boolean-trap-when-designing-react-components/" title="How to Avoid the Boolean Trap When Designing React Components" target="_blank">“How to Avoid the Boolean Trap When Designing React Components”</a> for the SpiceFactory blog. I recommend giving that a skim before continuing because this article will revisit some of the points I made back then.

The post got a lot of traction on the main React subreddit and was even featured on Tyler McGinnis’ newsletter. It was the <a href="https://mobile.twitter.com/DanicFilip/status/1210545475662819328/" title="Related Twitter Thread" target="_blank">5th most popular article of 2019 on his newsletter</a> – which I’m proud of! And since enough eyeballs saw the post, I’ve come across some questions and criticism.

I’ve been meaning to answer some comments, but I figured it’s more productive to compile everything in a followup which I finally got around to writing.

So here we go, in this post, **I’ll clear out 3 misconceptions and provide another benefit** of sticking to the advice outlined in the article.

## Misconception #1: This Won’t Scale!

Some people pointed out that if you have a `PrimaryButton` that can be `small`, `normal` or `large` this means you will end up with components such as `SmallPrimaryButton`, `NormalPrimaryButton` and `LargePrimaryButton`. And that this can expand to the point of absurdity.

I agree, that is indeed absurd and it _“doesn’t scale.”_

But, that’s not what I argued for in the article. The article argued for the **removal of booleans through the use of higher encapsulations and enums.**

Higher encapsulation – _via wrapper components_ – is one of the ways that we can achieve that. We don’t have to use it for every single combination.

We as developers can judge when it is appropriate to go with encapsulation or exposing the enum. It all depends on context!

In the example above, the `PrimaryButton` wrapper exists because it will be used often and because it is the most important distinction of the button. As for the size attributes, you would use the enum pattern to set it:

```javascript
<PrimaryButton size={ButtonSizes.SMALL} />
<PrimaryButton size={ButtonSizes.NORMAL} />
<PrimaryButton size={ButtonSizes.LARGE} />
```

And honestly, the value of `ButtonSizes.NORMAL` will likely be the default anyway.

Now, there’s nothing wrong with this either:

```javascript
<Button
  type={ButtonType.PRIMARY}
  size={ButtonSizes.NORMAL}
/>
```

But I argue that having the `PrimaryButton` abstraction is optimal as it communicates the intent of the component clearly and fast. Yes, _I could skim through a list of props_ to figure it out, but having `PrimaryButton` is a **faster approach.**

_It also leaves us with more options when it comes to searching the codebase and refactoring. (More on that later.)_

## Misconception #2: You’d Never Make the Original Mistake

Several commentators said that the opening example:

```javascript
<Button primary secondary>
  Primary or Secondary?
</Button>
```

…is something that would never happen. Implying that someone, most likely the developer, would catch it.

That’s likely the case. Though this was just that an opening example to a much broader set of concepts. It didn’t feel right that some people would dismiss the entire article over that. Even so, I don’t agree with this specific criticism.

**Why would we create APIs that allow for such absurd scenarios** and hope that a human would catch it?

If the mistake seen in the opening example makes it to the codebase then who knows how long it could stay there. If the original developer fails to catch this, then the only real way to catch this is through code review. (Maybe through some snapshot or e2e tests, but I think it is unlikely given the available tools.)

And even so:
- There are a lot of solo developers out there who don’t have this safety net.
- Many companies don’t practice code review as part of their process.
- We know that some code reviewers just skim through things.

If you’re working in a large team with a tight development process and culture that commits to quality, then you’re likely fine. (_Though in such a culture, I’m assuming a senior engineer wouldn’t allow such a bad API to exist in the first place._)

My point is that **if it could happen, it probably will.** So, why risk it, especially when there are better patterns available?

The opening example is a bit easier to spot because the booleans imply the opposite thing. What if it wasn’t so clear? The chances of this slipping through suddenly increase quite a bit.

It’s also important to keep in mind that good component APIs become even more important if you’re creating libraries that will be used across teams. Good component design should be intuitive.

## Misconception #3: Performance Impact

Several comments online asked whether creating these wrapper components could somehow cause performance issues.

I did a simple benchmark that shows 10,000 components (regular in test 1, wrapped in test 2) on the screen without <a href="https://web.dev/virtualize-long-lists-react-window/" target="_blank" title="Virtualize large lists with react-window">list virtualization.</a>

In these tests, I didn’t notice any difference in terms of average fps, memory consumed, or render time. I used Chrome’s CPU throttling to simulate a lower CPU-power device but both tests performed similar.

I know this benchmark isn’t definitive proof, but it’s also a pretty solid indicator that there are no real performance downsides.

Browsers are good at optimizing code at runtime, and the pattern seen in this example is rather straightforward from an optimization standpoint.

## Extra Benefit: Quicker and More Reliable Refactoring

Let’s say you introduce a new property that is mandatory whenever a `DangerButton` is used but is otherwise optional for other button types. This might even be a good moment to completely reimplement the `DangerButton`.

Since you’ve encapsulated it already, it will be an easy task for you. You can work directly on the implementation of `DangerButton` or quickly find all uses of it to add the required prop.

If you, however, followed the `<Button danger>` approach, you will have a much harder time, or at least waste of lot it.
