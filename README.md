<img height="300" width="100%" src="./assest/rnext-thumb.png"/>

# REACT & NEXT JS NOTE 🚀

> A hand note of my react & next js journey.....

<br>
<div align="center">

| Key Note  |                      |           |                           |
| --------- | -------------------- | --------- | ------------------------- |
| **Emoji** | **Description**      | **Emoji** | **Description**           |
| 🌴        | **Main Topic**       | 🏷️        | **Regular Note**          |
| 🌿        | **Main Category**    | 📌        | **Regular Note**          |
| 🍃        | **Sub Category**     | 💎        | **High Value info**       |
| 🍂        | **Sub-sub Category** | ✋        | **Stop! check the point** |
| 🎈        | **Step**             | 🎯        | **Focus**                 |

</div>

<!-- NO COMMENT -->

## Table of Contents

[🌴 Module 1. Getting started with React: Describing the UI](#-)

- [🌿 1.1 Introduction to React](#)
- [🌿 1.2 React Installation & Development Env](#)
- [🌿 1.3 How React works: Virtual DOM](#)
- [🌿 Basics of React Components](#)
  - [🍃 1.4 Your first component](#-)
  - [🍃 1.5 Importing & Exporting Components](#-)

<br>

## 🌴 Module 1. Getting started with React: Describing the UI

## 🌿 1.1 Introduction to React

**Understanding the Vue instance, data, methods, computed properties, and lifecycle hooks.** <br>
The Vue instance is at the core of Vue.js and serves as the root of every Vue application. It's responsible for managing the data, methods, computed properties, and lifecycle hooks of your Vue components.<br>

```
var app = new Vue({
  // Options
});

```

## 🌿 1.2 React Installation & Development Env

\***\*Understanding the Vue instance, data, methods, computed properties, and lifecycle hooks.\*\*** <br>
The Vue instance is at the core of Vue.js and serves as the root of every Vue application. It's responsible for managing the data, methods, computed properties, and lifecycle hooks of your Vue components.<br>

```
var app = new Vue({
  // Options
});

```

<!-- Chapter : 1.4 ---------------------------------------------------------------------------------------->

<div align="center"><h2>🌿 Basics of React Components</h2></div>

## 🍃 1.4 Your first component:

**1. Understanding Components in React**

Components are the core building blocks in React, combining HTML, CSS, and JavaScript into reusable UI elements. They enable the composition, ordering, and nesting of elements to create complete web pages or applications.

**Code:**

```
// Example of a simple component

export default function Profile() {
  return (
    <img
      src="https://i.imgur.com/MK3eW3As.jpg"
      alt="Katherine Johnson"
    />
  );
}

```

**2. Defining a Component**

- React components are JavaScript functions exported using export default.
- Component names must start with a capital letter and return JSX markup, which allows embedding HTML-like syntax in JavaScript.

**Code:**

```
// Example of defining a component
export default function Profile() {
  return (
    <img
      src="https://i.imgur.com/MK3eW3As.jpg"
      alt="Katherine Johnson"
    />
  );
}

```

**3. Using Components**

- Components can be nested within other components.
- They render to HTML elements in the browser and can be organized within the same file or in separate files for modularity.

Code:

```
// Example of using a component within another component
export default function Gallery() {
  return (
    <section>
      <h1>Amazing scientists</h1>
      <Profile />
      <Profile />
      <Profile />
    </section>
  );
}

```

**4. Best Practices and Pitfalls**

- Avoid defining components within other components for performance reasons.
- Data should be passed from parent to child components through props rather than nesting definitions.

**Notes:**
Remember, while components facilitate the creation of reusable UI elements, it's crucial to structure them wisely and adhere to best practices to maintain code quality and performance.

<!-- Chapter : 1.5 ---------------------------------------------------------------------------------------->

<div align="center"><h2>🌿 Basics of React Components</h2></div>

## 🍃 1.5 Importing & Exporting Components

**1. Root Component and File Organization**

The root component file in React houses primary components. Organizing components into separate files enhances modularity and reusability.

**Code:**

```
// App.js - Root component

import Gallery from './Gallery.js';

export default function App() {
  return (
    <Gallery />
  );
}

```

**2. Exporting and Importing Components**

To modularize components:

- Create a new file for the component.
- Export the component (default or named).
- Import the component into the file where it will be used.

**Code:**

```
// Gallery.js - Contains Profile (not exported) and Gallery (default export)

export default function Gallery() {
  // ... (uses Profile internally)
}

// App.js - Imports Gallery from Gallery.js
import Gallery from './Gallery.js';

export default function App() {
  return (
    <Gallery />
  );
}

```

**3. Default vs Named Exports**

**A file can have only one default export** but multiple named exports. To avoid confusion, some teams prefer using either default or named exports consistently within a file.

Code:

```
// Gallery.js - Contains both default and named exports

export default function Gallery() {
  // ... (default export)
}

export function Profile() {
  // ... (named export)
}

// App.js - Imports both Gallery (default) and Profile (named) from Gallery.js

import Gallery, { Profile } from './Gallery.js';

export default function App() {
  return (
    <Profile />
  );
}

```

**4. Exporting Multiple Components**

Utilizing named exports allows exporting multiple components from a single file, enhancing flexibility in component usage across the application.

Code:

```
// Gallery.js - Contains Gallery (default) and Profile (named) exports

export default function Gallery() {
  // ...
}

export function Profile() {
  // ...
}

// App.js - Imports both Gallery (default) and Profile (named) from Gallery.

import Gallery, { Profile } from './Gallery.js';

export default function App() {
  return (
    <Profile />
  );
}

```

**Recap:**

This section covered the root component, importing/exporting components, usage of default vs named exports, and exporting multiple components from a single file. It emphasized organizing components into separate files to enhance maintainability and reusability in React applications.
