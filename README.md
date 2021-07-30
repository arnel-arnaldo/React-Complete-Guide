# React - The Complete Guide

## Section 3: React Basics and Working with Components

1. Module Introduction
2. What are Components? And Why is React All About Them?
3. React Code is Written in a Desclarative Way
4. Creating a New React Project
   - Install React (_$ npx create-react-app react-the-complete-guide_)
   - Run React app (_$ npm start_)
   - Deleted unnecessary files from src folder; copied from repo the codes for App.js, index.css & index.js
5. Analyzing a Standard React Project
   - **index.js** is the first file that is run
   - **App.js** is the root (or main) component; it uses JSX expressions
6. Introducing JSX
   - **JSX** stands for JavaScript Xml
7. How React Works
   - Discuss how React transforms JSX expressions to JavaScript codes
8. Building a First Custom Component
   - create a folder to hold custom components
   - create a component called ExpenseItem.js
   - call the component from App.js with `<ExpenseItem></ExpenseItem>`
9. Writing More Complex JSX Code
   - There must only be ONE root element per return statement
10. Adding Basic CSS Styling
    - Create a CSS file called ExpenseItem.css under components folder
    - Apply the classes (using **className**) in ExpenseItem CSS file to ExpenseItem.js
11. Outputting Dynamic Data and Working with Expressions in JSX
    - use variables to store data; use `{_variable-name_}` in JSX expression
12. Passing Data via "props"
    - 'props' is short for properties
    - create expenses array in App.js; to be passed as props to ExpenseItem.js
13. Adding "normal" JavaScript Logic to Components
    - use [toLocaleString()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date/toLocaleString) and [getFullYear()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date/getFullYear) functions to date to display month, day and year.
14. Splitting Components into Multiple Components
    - create another custom component (ExpenseDate.js) that will render the expense calendar date; this will be called from ExpenseItem.js
15. Time to Practice: React and Component Basics
    - create another custom component (Expenses.js) that will render all expenses items; this will be called from App.js as `<Expenses items={expenses} />`. The component (Expenses.css) to style it will also be created.
16. The Concept of "Composition" ("children props")
    - introduction to React powerful **composition** model. Here is a link from ReactJS documentation that recommends using composition instead of inheritance [(Composition vs Inheritance)](https://reactjs.org/docs/composition-vs-inheritance.html) to reuse code between components.
17. A First Summary
18. A closer Look at JSX
19. Organizing Component Files
    - create two folders: Expenses and UI.
    - Expenses folder will contain all components related to Expenses while UI folder will contain all components that renders the display, i.e. Card.
20. An Alternative Function Syntax
    - use the arrow function (`const <function_name> = () => {}`) to write functions.
