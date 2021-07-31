# React - The Complete Guide

## Section 4: React State and Working with Events

1. Module Introduction
2. Listening to Events and Working with Event Handlers
   - introduces event handler (e.g. `onClick={clickHandler}`) on React.
   - the name inside the `{...}` is only pointing to the function and not executing the function.
3. How Component Functions are Executed
   - explains how components (which are really functions) work; they are rendered only <ins>once</ins> when called; any changes that happen on the UI will not be rendered or reevaluated.
4. Working with "State"
   - introduces the [**State Hook**](https://reactjs.org/docs/hooks-state.html) by calling a 'named import' called **useState** (`import { useState } from 'react'`)
   - `useState()` should only be called inside a function.
5. A Closer Look at the "useState" Hook
6. Adding Form Inputs
   - create new folder (NewExpense) under components
   - under this folder, the following new files (and its CSS counterparts) are created:
     - NewExpense.js(css) - add new expenses to the list.
     - ExpenseForm.js(css) - form that will render the inputs for new expenses.
7. Listening to User Input
8. Working with Multiple States
9. Using One State Instead (and What's Better)
10. Updating State that Depends on the Previous State
11. Handling Form Submission
12. Adding Two-Way Binding
13. Child-to-Parent Component Communication
14. Lifting the State Up
15. Time to Practice: Working with Events and State
16. Controlled Versus Uncontrolled Components and Stateless Versus Stateful Components
