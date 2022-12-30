---
title: Hands-on MERN Stack Web Development (Video Course)
seo_description:
promo_photo: /content/images/2019/mern-stack-development-course.png
date: 2019-04-01
tags:
---

After several months of work, I’m happy to announce that my second course, _**[Hands-on MERN Stack Web Development ](https://www.packtpub.com/web-development/hands-mern-stack-web-development-video)**_ is available on Packt. You can purchase the course and own it for life, or select a Mapt subscription to get access to all of Packt’s courses on-demand. (There’s a free 10-day trial. 😉)

## MERN Stack Course Overview

During the course you’ll build a full MERN Stack web application, front to back, from scratch. It’s an e-commerce shop that includes:
- Category-based product filtering.
- A shopping cart that is remembered across sessions and synced across tabs.
- “Passwordless” login and account creation. (Also known as the “magic link” pattern.)
- An admin-only area for user and product management.

The course runs at about 4 and half hours and is structured into 7 sections. The videos are anywhere from 4 to 12 minutes long.

I cover each part of the MERN stack individually at first, and then combine everything for a true “full-stack experience.” Each section sets of with a particular set of goals and challenges that we’ll overcome. You can skip ahead and read [the full list of topics we cover.](#The-Long-List)

If you’re only interested in React – and want to dive in deep – my [React course is a better resource.](/2018/hands-on-web-development-with-react-course)

## Teaching Style

This is my second video course and I’ve learn a lot from the feedback on my React web development course.

The basic idea stayed the same though:
- The videos are mostly a mix of talking and live coding, accompanied by slides when discussing theoretical concepts.
- Code files are included with the course.
  - There is also a [git repository](https://github.com/PacktPublishing/Hands-on-MERN-Stack-Web-Development) where each commit is tagged with the video it related to.
- Each video follows a similar pattern:
  - **Step 1:** Overview of the problem and formalization of the task.
  - **Step 2:** What are the technical challenges? Do we need to introduce a new concept?
  - **Step 3:** Code it out and discus the solution.
- Depending on where you buy the course, there will be a quiz at the end of some of the videos, to test if you’ve been paying attention.

My advice for consuming the content of the course is to watch it in chunks between 2 to 6 minutes and then pause and try writing some code yourself.

### Sound Quality

I’m not a native English speaker, but I’ve been told my accent is solid. I know that bad sound quality and/or a difficult accent can put people off. Here’s what you should know:
- The sound is recorded with a solid condenser microphone and pop-filter over it.
- My editor from Packt has worked on removing background noise and normalizing the audion volume.
- An introductory video at the bottom of the course landing page will give you a good idea of the sound quality and my accent.

## The Long List

**When it comes to Node and Express, you’ll learn:**
- How to setup a Node/Express project from scratch. (With Babel as your code transpiler and `nodemon` for hot file reloding.)
- All you need to know about Express middleware and write a couple of your own.
- How to use [Jest](https://jestjs.io/) and function mocking to test middleware and other callback-based modules.
- How to handle `GET`, `POST`, `UPDATE`, and `DELETE` requests.
- How to parse HTTP headers and body.
- How to create [RESTful APIs](https://en.wikipedia.org/wiki/Representational_state_transfer) and provide a full CRUD (Create, Read, Update, Delete) interface.
- How to implement passwordless authentication with [JSON Web Tokens.](https://jwt.io/)
- How to connect to MongoDB and manage schemas with `mongoose`.

**When it comes to MongoDB, you’ll learn:**
- How to run MongoDB from your local machine, inside a Docker container, and/or connect to one in the cloud.
- The differences between SQL and noSQL databases and what makes MongoDB unique.
- How to create collections and manage documents.
- How to manage references between documents and across collections.
- How to filter and aggregate data based on multiple criteria.

**And as for React, you’ll learn how to:**
- Bootstrap a new project with [Create React App.](https://github.com/facebook/create-react-app)
- Create React components and manage application state. Among other things this includes:
  - Input fields, forms and event handling.
  - Lists and dynamic item rendering.
  - Loading indicators and error states.
  - Other common UI components.
- Use lifecycle methods, render props, and Synthetic Events.
- Create Functional (Stateless) Components.
- Implement a callback-controlled data flow and when (and how) to perform state lifting.
- Understand the the virtual DOM, the reconciliation algorithm and diffing process.
- Implement simple typesafety with React PropTypes.
- Build a fully-functional, feature-rich SPA with:
  - Dynamic routing via [React Router,](https://reacttraining.com/react-router/)
  - support for multiple roles, and
  - granular access control via feature/permission flags.
- Setup Unit and Snapshot Testing with Jest.

**You can also expect to:**
- Gain insight into the economics of full-stack development and gain valuable industry insight.
- Learn about refactoring and improving the quality of your code.
- Gain experience with CSS Modules and working with the Flexbox model.
- Learn how to build reusable software – especially when it comes to reusable React components.

So, go ahead and **[check it out!](https://www.packtpub.com/web-development/hands-mern-stack-web-development-video)**

## What I Left Out

There are also some things that I’ve left out and that you might have expected would be in the course. I think it’s fair to mention those:

- **The React Context API** – it’s not something you need at the current level. When you need it, you’ll be able to read up on it and learn it by yourself.
- **React Hooks** – at the time of recording, they were still in early beta. I’m planning on recording a free supplement on the topic. Stay tuned!
- **MERN.io Boilerplate** – this is a popular starter kit that does get mentioned in the course. If decided not to use it because I see value in learning by start from scratch. Once you complete the course you’ll be able to figure out how to use the boilerplate on your own.
- **Redux** – it’s a powerful library for state management. But since there is already an amazing [free course by Dan Abramov, the creator of Redux](https://egghead.io/courses/getting-started-with-redux) I think my time was better used to focus on other things.
