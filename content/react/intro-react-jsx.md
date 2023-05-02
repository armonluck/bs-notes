# Unit 3 Kickoff on May 2nd, 2023

## Intro to React
![React icon](https://upload.wikimedia.org/wikipedia/commons/thumb/a/a7/React-icon.svg/1200px-React-icon.svg.png)

### What is React?

- React is a JavaScript library for creating user interfaces (UI)
- Based around the idea of reusable components and providing data to them
- Created by Facebook (aka Meta)
- There are many libraries similar to React, but React is currently the most popular in the industry

### Where does React fit?

- React is **great** for creating complex, rich, dynamic user interfaces for web applications
- These interfaces can:
  - Display changing data to the user
  - Respond to user inputs and actions

### Features of React

- **Components**: centered around resuable UI components
- **State Management**: structured approach to managing application data
- **DOM Management**: we (developers) declare how we want it to look and React updates the DOM for us
- **Flexible**: used on web or mobile

### Why use React?

- Developing in React requires a shift in mindset, yet it has ~15 million npm downloads weekly in the last month (as of March 2022)
- Structuring code in encapsulated **components** increases:
  - Reusability
  - Modularity
  - the ability to unit test our UI
- React is **fast**
- React is ***flexible***:
  - Renders client or server-side
  - Used on web or mobile
  - Made so that incremental adoption is possible
- React has good **tooling**
  - `create-react-app` scaffolding
  - React devtools chrome extension
  - Instructive error messages

### Building Apps in React

- Focus on building a library of UI components, rather than a set of web pages
- Developers define components that are small (but complete) sections of UI
- Once defined, we wire these components together to build hierarchically larger interfaces

### Chunking a Design Into Components

- A designer hands us a design mockup
- Slice up hte design into UI components
- Define each component
- Build/Compose each UI screen using the components we defined
- *Note how smaller components come together to form larger components*

### Creating React Components

- In React, components are the building blocks of the interface
- Each component is a piece of UI that is:
  - Independent
  - Reusable
  - Encapsulated
- Primary job of a component is to output what that piece of UI looks like when it is rendered

### Working with Components

- There are 2 main steps to using components
  1. Define a component
  2. Use instances of that component
- Similar to functions - define a component once and reuse an unlimited number of times

### Component Definitions

- Components can be defined as classes or functions
- All components must return some part of the U

    function HelloMessage() {
        return (
            <div>Hello World!</div>
         )
    }

- Component definitions are like blueprints for that component
- All component definitions must be capitalized
