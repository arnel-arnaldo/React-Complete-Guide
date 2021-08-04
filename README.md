# React - The Complete Guide

## Section 5: Rendering Lists and Conditional Content

1. Module Introduction
2. Rendering Lists of Data
   - use `map()` function to dynamically render `ExpenseItem ... />` in Expenses.js.
3. Using Stateful Lists
   - put expenses array outside of the App() function.
   - use **useState()** to monitor the state of the added expenses using this:
     - `const [expenses, setExpenses] = useState(DUMMY_EXPENSES)`
   - the add expense handler is rewritten as:
     - `const addExpenseHandler = (expense) => { setExpenses((prevExpenses) => { return [expense, ...prevExpenses] })}`
4. Understanding "Keys"
   - always use `key={...}` when mapping out list of items to prevent execution delays or bugs.
5. Time to Practice #1: Working with Lists
   - filter the list of expenses using the **filter()** function in Expenses.js: `const filteredExpenses = props.items.filter((expense) => { return expense.date.getFullYear().toString() === filteredYear })`
6. Outputting Conditional Content
   - use this: `let expensesContent = <p>No expenses found.</p>`
   - and this: `if (filteredExpenses.length > 0) { expensesContent = filteredExpenses.map((expense) => ( <ExpenseItem key={expense.id} title={expense.title} amount={expense.amount} date={expense.date} /> )) }`
7. Adding Conditional Return Statements
8. Time to Practice #2: Conditional Content
   - add a conditional content by initially hiding the new expense form and displaying instead a button that says "_Add New Expense_". When this button is clicked, the new expense form is displayed with buttons "_Cancel_" and "_Add Expense_" included.
9. Demo App: Adding a Chart
   - add a **Chart** folder that will contain all JS and CSS components pertaining to the chart.
10. Adding Dynamic Styles
    - use the `style={{ height: barFillHeight }}` where barFillHeight is dynamically computed based on the props value and maxValue passed as props.
11. Wrap Up and Next Steps
    - add another file, **ExpensesChart.js**, that will contain and compute values for chart data points; this will call **Chart.js**.
