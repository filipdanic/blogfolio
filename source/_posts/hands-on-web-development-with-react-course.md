---
title: Hands-on Web Development with React (Video Course)
seo_description: Hands-on web development with React is a video course by Filip Danić. Aimed at newcomers who want to learn React.js
promo_photo: /content/images/2018/react-web-development-course.png
date: 2018-09-28
categories: engineering

---

After nearly 200 hours of work, my first video course is available! _**[Hands-on Web Development with React](https://www.packtpub.com/web-development/hands-web-development-react-video)**_ is available via Packt Publishing and you can actually jump into the course for free [via Mapt.](https://www.packtpub.com/mapt/video/web_development/9781789343915) (Packt’s on-demand course platform.)

## The Elevator Pitch

You’ll learn how to build a ReactJS web application / SPA from scratch. We’re going to build a job board app where:
- Visitors can see job postings and search through them via a global search bar.
- Registered users can add/edit postings (if they’re on a `paid plan`) and view stats on their existing/old ones.
- Admin users can edit postings and view global analytics in the form of a nice chart.

Along the way, you’ll also learn about `css-in-js`, mocking, functional programming, and pick up some general software engineering wisdom.

The course is structured into 7 sections that span across ~4.5 hours. Each with a particular set of goals and challenges that we’ll overcome. You can skip ahead and read [the full list.](#The-Long-List)

_Note: The course is made with React 16 in mind, but works with `15.x.x`. The guide will still be relevant once React 17.0.0 is released._

**Style & Approach:**

- The videos are mostly a mix of talking and live coding, accompanied by slides when discussing theoretical concepts.
- Code files are included with the course.
  - There is also a [git repository]( https://github.com/PacktPublishing/Hands-on-Web-Development-with-React) where each commit is tagged with the video it related to.
- Each video follows a similar pattern:
  - **Step 1:** What’s the problem? How are we planning to solve it?
  - **Step 2:** What technical concepts do we need?
  - **Step 3:** Let’s code it out and discus along the way!
- The sound is recorded with a solid condenser microphone and pop-filter.
  - An introductory video at the bottom of the course landing page will give you a good idea of the sound quality and my accent. :)
- There’s a quiz within and at the end of some of the videos, to test if you’ve been paying attention.

Note: if you’ve seen my [YouTube or Twitch videos](https://www.youtube.com/channel/UClctBvKpOUts0_B_kvooo_w) then you should know that the approach in this course is different. The videos are between 4 to 10 minutes long and highly focused. Unlike the streams which last for hours and are fairly _“free form.”_

My advice for consuming the content of the course is to watch it in chunks between 2 to 6 minutes and then pause and try writing some code yourself.

## The Long List

**You will:**
- Learn how to bootstrap a React application with Create React App.
- Create React components and manage application state.
  - Forms and event handling.
  - Lists and dynamic item rendering.
  - Loading indicators and placeholders.
  - Other common UI components.
- Understand the why and how behind core React concepts and common patterns.
  - Lifecycle methods.
  - React PropTypes.
  - State lifting and prop drilling.
  - Callback-controlled data flow.
  - Functional (Stateless) components.
- Learn patterns for building reusable ReactJS components.
- Learn how to communicate with a real server, as well as local mocks.
- Use CSS-in-JS with `styled-components`.
- Build a fully-functional, feature-rich SPA with:
  - Dynamic routing via `react-router-dom`,
  - support for multiple roles, and
  - granular access control via feature/permission flags.
- Learn core functional programming concepts and how they apply to working with React.
  - Map, filter, reduce!
  - Pure functions.
  - Immutability.
  - Higher order functions and higher order components.
- Practice Unit and Snapshot Testing with Jest, a JavaScript test runner.
- Figure out how to configure your build and deploy it to production.
- Learn about the basics of React’s internals:
  - The virtual DOM.
  - The reconciliation algorithm and diffing process.

## What I Left Out

There are also some things that I’ve left out and that you might have expected would be in the course. I think it’s fair to mention those:

- The React Context API – it’s not something you need at a junior/intermediate level. When you need it, you’ll be able to read up on it and learn it by yourself.
- Render Props – it’s considered an “advanced pattern”, but this is mainly to it being a new, shiny tool in a React developer’s arsenal. When you need them, you can learn them on your own. They’re not that important at this stage.
- Redux – it’s common for instructors to bundle Redux into a React course. The two technologies are used widely. However, I feel that Redux is it’s own topic and I am against learning it before you have a good grasp of React.
 - Once you understand the pains of state management, you’re ready to start exploring Redux on your own. There’s also a ton of free resources that would explain it better than I would. [Including one by Dan Abramov, the creator of Redux.](https://egghead.io/courses/getting-started-with-redux)
