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
   - add listeners for each input, e.g for `<input type='text' onChange={titleChangeHandler} />`
   - the function that handles the event (i.e. titleChangeHandler) will be called with a parameter called **event**(or **e**) which can be used to get the input value.
8. Working with Multiple States
   - create 3 `useState()` corresponding to the 3 inputs in ExpenseForm.js
9. Using One State Instead (and What's Better)
   - The 3 `useState()` can be re-written as:
     `const [userInput, setUserInput] = useState({ enteredTitle: '', enteredAmount: '', enteredDate: '', })`
     and the event handler function will be re-written as:
     `const titleChangeHandler = (e) => { // setEnteredTitle(e.target.value) setUserInput({ ...userInput, enteredTitle: e.target.value, }) }`
10. Updating State that Depends on the Previous State
    - use this instead if updating a state depends on a previous state:
      `setUserInput((prevState) => { return { ...prevState, enteredTitle: e.target.value} })`
11. Handling Form Submission
    - use `onSubmit={}` to get the input values when the form is submitted.
    - include `e.preventDefault()` on the submit form handler to prevent the form from reloading when the form is submitted.
    - store the entered values as:
      `const expenseData = { title: enteredTitle, amount: enteredAmount, date: new Date(enteredDate), }`.
12. Adding Two-Way Bindin
    - Two-way binding simply means we don't just listen to inputs but we also pass values to inputs; this is achieved by adding a `value={...}` argument to input controls.
13. Child-to-Parent Component Communication
    - data can be transmitted from child to parent component by utilizing props to receive a function from the parent component which is called from the child component. This concept is similar to "Lifting the State Up"
14. Lifting the State Up
15. Time to Practice: Working with Events and State
    - use the lessons learned on this Section to add a component that lets user pick a year and filters the expenses using that year.
16. Controlled Versus Uncontrolled Components and Stateless Versus Stateful Components
