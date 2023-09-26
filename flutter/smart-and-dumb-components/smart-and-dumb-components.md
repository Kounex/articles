# Concept of: Smart and Dumb components in Flutter

In our Flutter development journey, we will eventually start to put more and more thought into the structure of our codebase. We will have to decide where which part of our application code resides and how to do that consistently. It is mainly driven by seperation of concern so we will start of by seperating business logic from our UI code and from there move on to other, more in-depth use cases. Eventually we will think about how precisely we slice every aspect of our app to make it readable, understandable and therefore maintainable and scaleable. In this blog post I will focus on reiterating over an existing concept to think about for our codebase structure journey: Smart and Dumb components.

## What is this concept about?

As the name already indicates, it's about splitting components, in our case widgets, into smart and dumb ones. Therefore those interacting with the business logic part of our app and compositing / delegating other widgets (smart components) and those not knowing anything about the overall app / feature logic and only focus on presenting given information and executing what they have been provided on certain events (dumb components). This will drastically help us to design and structure our widgets - especially when talking about where to put and later on find aspects of our widgets. This will speed up the development process while working on some of our core goals: readability and maintainability.

## Top down view