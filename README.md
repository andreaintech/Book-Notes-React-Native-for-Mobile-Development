# Book Notes React Native for Mobile Development :books:

This are my taking notes of Book: [React Native for Mobile Development - Harness the Power of React Native to Create Stunning iOS and Android Applications](https://www.amazon.com/-/es/Akshat-Paul/dp/1484244532)

Authors:
- [Akshat Paul](https://www.akshatpaul.com/)
- [Abhishek Nalwaya](http://nalwaya.com/)

# Chapter #1 - Learning the Basics: a Whistle-stop tour of React :books:

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

![image](https://user-images.githubusercontent.com/20091777/125729611-b5fae65a-dcf7-4650-951e-de42a9757fd3.png)
_Figure 1-1. Virtual DOM and diffing algorithm operations_

Manual DOM manipulation is messy, and keeping track of the previous state of the DOM is very hard. As shown in Figure 1-1, React solves this problem by keeping 
two copies of a VDOM. Next, a diffing algorithm is applied on these two VDOMs, which essentially checks for the changes that occurred and returns a stream of DOM 
operations. These DOM operations are then applied to the actual browser DOM.

**How a VDOM works:**
In React, every component has a state; this state is likely observable. Whenever there is a change in state, React essentially knows that this change requires a rerender. When the application state changes, it generates a new VTree; once again the diffing algorithm shares the DOM paths for required changes, as shown in Figure 1-2. 
**This results in keeping manual DOM manipulation to a minimum**

![image](https://user-images.githubusercontent.com/20091777/125730183-5d9b2ef9-cbfc-48bf-90e2-2468067ef17c.png)
_Figure 1-2. Components with virtual VDOM_

This feature of VDOM is not just important, but a killer feature of React. DOM access is super slow, and honestly speaking, the world has made it worse by hitting the DOM again and again in most applications. 

To make your application fast, you should access the DOM as little as possible, and this is beautifully handled by the implementation of VDOM. You won’t notice this with a small and trivial application, but once your app grows to include thousands of DOM elements all trying to get updated, **React will not let your performance suffer.**
_______________________
**One-Way Data Flow**

React is primarily the V in an MVC pattern, but before you dive into the idea of one-way data flow in React, you must understand the challenges of MVC frameworks. One of the biggest challenges of an MVC framework is managing the view. As you know, the view component of the MVC framework is mainly the DOM representation. It is simple when you write code that interacts with the DOM, but it is very complicated for the framework to handle various DOM manipulations.

Traditional MVC views generally encompass a lot of heavy UI, and as the data change even for a tiny element, it eventually rerenders the app again, and the cycle 
continues. The reason for this is that typically most of these MVC frameworks follow two-way data binding.

![image](https://user-images.githubusercontent.com/20091777/125839676-f523dcf5-acbe-440d-92e8-0a70062de4f6.png)
_Figure 1-3. Two-way data binding_

In JavaScript, data change in memory and they are bound to a view in the UI, which means that when data are modified in JavaScript, which is in memory, the data will be changed in the UI as well. In return, when data change in the UI (i.e., the DOM) by clicking a button or any other event, they get updated in memory also, keeping 
the two in sync.

However, in real-world applications, problems arise when you have a fairly complex and large application with multiple views representing data in one of your models.  As you add more models and more views, this two-way data binding ends up as spaghetti with every change in data added to the pot, which sometimes even ends up in an infinite event loop where one view updates a model, which in turn updates a view, and so on.

![image](https://user-images.githubusercontent.com/20091777/125840047-862be27e-540d-4021-8fce-7a2be8d5aaa9.png)

_Figure 1-4. Unwanted spaghetti relationship_

React follows one-way data flow to keep things simple.

![image](https://user-images.githubusercontent.com/20091777/125840370-778e35ed-79ff-4549-8f87-f526bef13d9c.png)

_Figure 1-5. React Native’s one-way data flow_

**It is based on the concept of separation of concerns (SoC).** This is a design principle in computer science in which an application or program is divided into distinct sections, each addressing a single or specific concern. The value of this design principle is that it simplifies development to create a maintainable and scalable application. **This leads to modularized code where an individual section can be reused, developed, and modified independently. This makes so much sense and is indeed an example of intelligent thinking.**

_______________________
**Installation and Setup**

React is just a node module, there are lot of different ways to set up a React project.
We can include React in existing projects using npm or yarn and start using it. If you are starting a new project, we recommend using the create-react-app npm package.

**create-react-app** is an out-of-the-box command-line interface (CLI) created by Facebook that creates a basic structure for the React app and takes care of ES7+ translation though Babel and Webpack. You don’t need to focus on configuration; instead you can focus on writing React code.

You can also check its github repo from here to look at its [documentation](https://www.npmjs.com/package/create-react-app).

We simply set it up for our development environment with the following command to install create-react-app:

    npm install -g create-react-app

_This command installs create-react-app globally._

Now that we have installed create-react-app globally, navigate to the directory where you want to create a project and run the following command:

    create-react-app <application_name>

We are all set to start working with React, but before we create our first app we recommend that you install React Developer Tools, a very useful Chrome extension that allows you to inspect the React component hierarchy in the Chrome browser. This tool can help boost your productivity. 

Click [here](https://chrome.google.com/webstore/detail/react-developer-tools/fmkadmapgofadopljbjfkapdkoienihi) to install React Developer Tools.

_______________________
**Create a Hello World Application**

Now let’s create a Hello World project. This command will install the essential packages and set up our React project.

    create-react-app hello-world

Running that command installs the dependencies needed to build your project, and it generates the initial project structure. Create React App installs the latest version of React and React-DOM, as well as the latest version of react-scripts, a development dependency that manages all other development dependencies that include starting, testing, and building your app. Create React App uses Webpack and Babel under the hood, but it generates only the files you need to work on your React project.

Traverse into the directory using your terminal or command prompt to play around with this application using the following commands:

    cd hello-world

    yarn start

It will automatically open http://localhost:3000/ in your default web browser and you can see the first page of our app.

_______________________
**Introduction to Components**

Components are the smallest units in React application development; they are indeed the most fundamental part of React. 
React is a library for building UIs and components are the key for creating any UI in React.

You might think of it as widgets that you can plug in anywhere.

These components define how DOM elements are created and how users can interact with them. The whole concept of components is that they are totally encapsulated, making them easy to test and reuse.

![react-code](https://user-images.githubusercontent.com/20091777/126711463-3e1f60a4-20b9-411f-8254-a7424dad11d7.png)

This is the main App component. As you can see, it’s just a JavaScript file that contains some HTML code. If you have been building software for some time, you know 
it is a best practice to keep your HTML and JavaScript code separate. Looking at this example, it goes against this fundamental best practice.

The reason this best practice exists is to decrease coupling and increase cohesion, which means we write the UI in HTML and logic in JavaScript. The challenge with this approach is that we can only attach behavior to HTML through HTML elements (like ID, class, etc.). 

A library like jQuery is a good example of this. As your files grow, it becomes difficult to manage and test your code. 

**React components solve this problem very well. It lets you create JavaScript objects using HTML syntax. Components serve two purposes: templates and display logic. Therefore, markup and code are tied together intimately. ** 

Display logic often is quite complex and to express it using template languages does become difficult. The best way to solve this problem is to generate HTML 
and components from JavaScript itself. React JSX solves these problems with its HTML- type syntax by creating React tree nodes.
