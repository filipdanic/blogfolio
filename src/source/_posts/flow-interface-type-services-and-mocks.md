---
title: Flow’s Interface Type, Services, and Mocks
seo_description: How to use Flow’s Interface Type to create Interfaces for Classes, Services and Mocks.
promo_photo: /content/images/2018/flow-interface-type.jpg
date: 2018-09-13
tags:

---

The `interface` is a well-known concept in the OOP world. If you’ve done a bit of Java in school, you know what it is. In the JavaScript world, we’re in desperate need of some of these basic concepts. But, there’s not enough solutions out there that get the job done well ***and*** have a low barrier to entry.

For example, I’ve worked with the [Google Closure Compiler](https://github.com/google/closure-compiler/) and [TypeScript.](https://www.typescriptlang.org/) For an existing project, both are a massive investment that’s hard to integrate. Yes, they provide *many other benefits* that potentially justify the cost – *but that’s not our topic right now!*

For now, we just want an `interface`. And maybe some opt-in type safety? [JSDoc annotations](http://usejsdoc.org/) can do a lot of good for a small cost. But, the tooling provided by Facebook’s Flow is even better – at arguably the same price of JSDoc, if you’re already using Babel!

[Flow](https://flow.org/en/) has a much lower barrier to entry. It took me 5 minute to install and setup everything [following their guide.](https://flow.org/en/docs/install/) And now I’m ready to use `@flow` where I need it – adding it gradually to the codebase!

<figure class="blog-post-image"><img src="/content/images/2018/flow-interface-type.jpg" alt="Ceramic tea cups" /><figcaption>The cup interface, implemented in various ways. Photo by rawpixel via Unsplash.</figcaption></figure>

## Interface Types and Usage in Flow

An `interface` is a group of related methods with empty bodies that define their arguments and return type. Consider the Vehicle interface.

```javascript
/* @flow */
interface Vehicle {
  currentSpeed: number;
  speedUp(amount: number): void;
  slowDown(amount: number): void;
  getCurrentSpeed(): number;
}
```

```javascript
/* @flow */
interface Aircraft {
  currentAltitude: number;
  increaseAltitude(amount: number): void;
  decreaseAltitude(amount: number): void;
  getCurrentAltitude(): number;
}
```

And then have your classes _implement_ them.

```javascript
/* @flow */
class RobotCar implements Vehicle {
  currentSpeed = 0;
  speedUp(amount: number) {...};
  slowDown(amount: number) {...};
  getCurrentSpeed(amount: number) {...};
}
```

```javascript
/* @flow */
// implement multiple interfaces!
class RobotCopter implements Vehicle, Aircraft {
  currentSpeed = 0;
  currentAltitude = 0;
  speedUp(amount: number) {...};
  slowDown(amount: number) {...};
  getCurrentSpeed(amount: number) {...};
  increaseAltitude(amount: number) {...};
  decreaseAltitude(amount: number) {...};
  getCurrentAltitude() {...};
}
```

Fairly straightforward, don’t you think?

### Generics

Although I’ve yet to use generics for something non-trivial, I am comfortable in knowing that Flow supports them. In the context of interfaces, it’s as simple as:

```javascript
/* @flow */
interface MyInterface<A, B, C> {
  property: A;
  method(val: B): C;
}
```

## Interfaces, Services and Mocks

Let’s say you’re building an app that integrates with many different third-party vendors. For example, financial institution such as banks.

You expect you might have different variants of some `FinancialService`. They’re all meant to have the same methods, but their implementation varies and they communicate with different vendors.

Having a `FinancialService` interface and having your `UnityBankService` and `CapitalTwoService` classes implement them, would allow you to have a consistent API.

Now, if you decided to call a method such as `_.getAccountBalance(accountId)`, you won’t really have to care about the underlying class.

> **You’re programming to an interface.**

When it comes to _mocking data_, interfaces also make life easier. Let’s say none of the classes above are implemented – but we need mocks for our demo. Or maybe their dependency on third-party vendors makes it hard to have automated unit tests.

Well, let’s just make a `MockFinanceService` that implements `FinancialService`. Then, we can use `.env` configs to specify what we want to be used:

```javascript
const service: FinanceService =
  config.useMocks || config.isTestEnv ?
  MockFinanceService :
  getImplementationClass();
```

It’s refreshing to see that programming in JavaScript is becoming much better (and more mature!)
