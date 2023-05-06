# Intro to [React](./system6.md) & JSX

![React icon](https://upload.wikimedia.org/wikipedia/commons/thumb/a/a7/React-icon.svg/1200px-React-icon.svg.png)

## Intro to React

### What is React?

- React is a JavaScript library for creating user interfaces (UI)
- Based around the idea of reusable components and providing data to them
- Created by Facebook (aka Meta)
- There are many libraries similar to React, but React is currently the most popular in the industry.
  - *May later see View and Angular*

#### Where does React fit?

- React is **great** for creating complex, rich, dynamic user interfaces for web applications
- These interfaces can:
  - Display changing data to the user
  - Respond to user inputs and actions

#### Features of React

- **Components**: centered around reusable UI components (hero banners, lists, cards, etc.)
- **State Management**: structured approach to managing application data
- **DOM Management**: we (developers) declare how we want it to look and React updates the DOM for us
- **Flexible**: used on web or mobile

#### Why use React?

- Developing in React requires a shift in mindset, yet it has ~15 million npm (node package manager) downloads weekly in the last month (as of March 2022)
- Structuring code in encapsulated **components** increases:
  - Reusability
  - Modularity
  - the ability to unit test our UI
- React is **fast**
  - *spoiler* due to the VDOM (Virtual DOM)
- React is ***flexible***:
  - Renders client or server-side
  - Used on web or mobile
  - Made so that incremental adoption is possible (you can pick and choose what you want to add to your application)
- React has good **tooling**
  - `create-react-app` scaffolding
  - React devtools chrome extension
  - Instructive error messages

### Building Apps in React

- Focus on building a library of UI components, rather than a set of web pages

  > React uses a single page of HTML, but can feel like a multi-page website through *routing*

- Developers define components that are small (but complete) sections of UI
- Once defined, we wire these components together to build hierarchically larger interfaces

#### Chunking a Design Into Components

- A designer hands us a design mockup
- Slice up the design into UI components
- Define each component
- Build/Compose each UI screen using the components we defined
- *Note how smaller components come together to form larger components*

### Creating React Components

#### React Thinks in Components

- In React, components are the building blocks of the interface
- Each component is a piece of UI that is:
  - Independent
  - Reusable
  - Encapsulated
- Primary job of a component is to output what that piece of UI looks like when it is rendered

#### Working with Components

- There are 2 main steps to using components
  1. Define a component
  2. Use instances of that component

- Similar to functions - define a component once and reuse an unlimited number of times

#### Component Definitions

- Components can be defined as classes or functions
- All components must return some part of the UI
- Component definitions are like blueprints for that component
- All component definitions must be capitalized

#### Using & Reusing Components

- Using a component as a blueprint, we can create unlimited **instances** of that component
  - e.g. we can have many chairs built from the same blueprint
- We *instantiate* a component using HTML-like syntax
  - `<HelloMessage />`

#### Rendering Components to the Page

- We do **NOT** need to call `render()` for each component in our app
- Typically, the app will hae one top-level component that is built from all the smaller components that make up our app
- We only need to call `render()` once, to put that top-level component on the page
-

### `create-react-app`

- `create-react-app` is a scaffolding tool to easily set up new React projects
- Exists in Node as an npm package
- Created by Facebook to improve the developer experience
- Also has a [great user guide](https://create-react-app.dev/docs/getting-started/)

#### Node Overview

- Node is a program that allows us to run JavaScript outside of a web browser
- Built on Google's Open Source V8 JavaScript engine: written in C++, used in Google Chrome
- The V8 engine is an "interpreter" that executes JavaScript code
- Node lets us run JavaScript in a terminal
- Node introduces the possibility of using one language for the full stack

#### What is npm?

- **N**ode **P**ack **M**anager
- Node's functionality is extended by libraries
- npm is a repository (repo) of Node libraries
- Provides a command line interface for installing libraries

#### Managing Dependencies with package.json

- `create-react-app` can be started using:
    `$ npm start`
- A file called `package.json` holds info about ALL libraries required for the project
- Install additional package dependencies
  - Installing packages locally:
    `$ npm install <package-name>`

#### `create-react-app`: Behind the Scenes

- `create-react-app` is a package that will quickly scaffold (build initial files, structure, or starting point for the application) a React project for you
- When initializing a project using `create-react-app`, a git repo is initialized for you (no need to run a `git init`)
- `create-react-app` also generates a `.gitignore` file for you in the root directory of the project
- Directories and files listed in the `.gitignore` file will not be tracked by version control

- The React project that was scaffolded by `create-react-app` contains some starter directories and files
- `create-react-app` comes pre-packaged with a package manager, **npm** by default or **yarn** if you have installed it globally
- Use npm as a package manager in a project scaffolded using `create-react-app`, delete the `yarn.lock` file if you see it in your folder

### My First Component

- `npx create-react-app my-first-app`
- In `index.js` of the project src folder, paste in the code to the right
- Run `npm start` from inside your project directory, where the package.json file is
- We just created a class based component

#### Class Based Component

- A class component must have 2 things to work properly:
  1. Must extend the Component class within the React library
    `class App extends React.Component`
  2. Must return JSX inside of a render method

- By extending the Component class, we hve access to many predefined methods and properties

#### Functional Component

- Essentially, just a JS function
- In order to be a component, the function must return JSX
- Both examples are valid functional components

***

## JSX & The Virtual DOM

### The Virtual DOM

#### What is the Virtual DOM?

- React holds a virtual representation of the DOM in memory
- Virtual means a tree of JS objects that represent the "Actual DOM" that a viewer sees in the browser
- when React is used to modify components, we are modifying the virtual DOM, not the "Actual DOM"
- React then compares the Virtual DOM and the Actual DOM and then changes only the elements that need to be updated, leaving the rest alone

- Modifying the DOM directly is a costly operation, degrading the performance of the application
- Keeping the stated in the DOM leads to confusion

#### React Elements

- Virtual DOM is a tree of *ReactElements*
  - these are just Plain Old JavaScript Objects (POJOs)
- Each element in the virtual DOM is represented by a corresponding element on the page

### JSX

#### What is JSX?

JSX is a syntax extension to js that allows JavaScript and HTML to be mixed. It looks like a **templating language** but has full power of JS.

- JSX is used to describe what our components should look like
- Commonly used in a functional components' return statement
- JSX requires preprocessing to convert to standard JavaScript the browser understands
  - A browser cannot directly understand JSX

props = properties

- E.g. an `<a>` tag can have attributes/properties such as `id=""`, `class=""`, `href=""`, `onclick=""`, etc.

`React.createElement('a', { id: "", className: "red-anchor", href: "https://www.google.com", onClick: callAFunction});`
