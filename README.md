# Book Notes React Native for Mobile Development :books:

This are my taking notes of Book: [React Native for Mobile Development - Harness the Power of React Native to Create Stunning iOS and Android Applications](https://www.amazon.com/-/es/Akshat-Paul/dp/1484244532).
Authors:
- [Akshat Paul](https://www.akshatpaul.com/)
- [Abhishek Nalwaya](http://nalwaya.com/)

# Chapter #1 :books:

**According to the official documentation, React is a JavaScript (JS) library (not framework) for creating user interfaces (UIs).** 

It was built in a combined effort by teams from Facebook and Instagram. React was first introduced to the world in 2013, and has taken it by storm, with community-wide acceptance and the benefit of being the technology at the heart of Facebook. 

According to official documentation, some consider React to be the V in a model-view-controller (MVC) framework, because React makes no assumptions about the rest of the technology stack used. 

You can use whatever technology you wish and you can create a single section of your app with React or React Native; you can also conveniently make changes in an already created application by incrementally adding React to it.

_______________________
**React came into existence because its creators were faced with a significant problem:**

how to build large applications in which data change frequently. This problem occurs in almost any real-world application and React was created from the ground up to solve it.

_______________________
**The following are some of the advantages of choosing React for your next project:**

• React uses JavaScript extensively: Traditionally the views in HTML are separated from the functionality in JavaScript. With React, components are created and there is one monolithic section where JavaScript has intimate knowledge of your HTML.

• Extendable and maintainable: Components are formed by a unified markup with its view logic, which actually makes the UI easy to extend and maintain.

• Virtual DOM: React applications are blazing fast. The credit for this goes to the virtual DOM and its diffing algorithm.

• One-way data flow: Two-way data binding is a great idea, but in real- world applications it produces more pain than benefit. One of the common drawbacks with two-way data binding is that you have no idea how your data get updated. With one-way data flow, things are simple: You know exactly where data are mutating, which makes it easier to maintain and test your app. 

_To have a strong foundation with a new technology, it’s necessary to understand its core concepts._

_______________________
**Virtual DOM**

In all web applications one of the most expensive operations from which an app suffers is mutating the DOM. To solve this problem, React maintains a virtual representation of the DOM (as shown in Figure 1-1), which is called Virtual DOM (VDOM). 

Along with a diffing algorithm, React is able to compute the data against the actual DOM and only update the part of the DOM that is changed. 

The amount of change is therefore less, which leads to a blazing fast application. In the beginning of your application you might not see it, but as your project balloons to greater complexity (which usually happens in real-world apps), you will begin to see the benefits of a snappy experience for users.
