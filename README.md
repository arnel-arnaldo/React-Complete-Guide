# React - The Complete Guide

## Section 8: Time to Practice: a Complete Practice Project

1. Module Introduction
   - this is section that will apply all the concepts learned from past sections; new concepts will be introduced as well.
   - the app is about adding username and age to a list (open doc folder for images).
   - delete the src folder from Section 7.
   - delete the package.json and package-lock.json.
   - copy the new src folder from Section 8 (master).
   - copy the new package.json from Section 8 (master).
   - run npm install to recreate dependencies (node_modules) folder.
2. Adding a "User" Component
   - map out components that are required:
     - username / age entry form
     - button to Add User (UI component)
     - card to display list of added users
     - modal form that displays invalid input
     - OK button
   - create **Components** folder that will contain the following subfolders:
     - **UI**
     - **Users** (contains user related components)
       - **AddUser.js** - put the codes for adding user logic; return `<Card>...</Card>`
3. Adding a Reusable "Card" Component
   - under UI folder, create **Card.js** and **Card.module.css**.
   - in Card.js, use the `<div ...>{props.children}</div>` to render all the child components (`<Form>...</Form>`) returned by AddUser.js.
   - under Users folder, add **AddUser.module.css**.
4. Adding a Reusable "Button" Component
   - under UI folder, create **Button.js** and **Button.module.css**.
   - in Button.js, use the `<button ...>{props.children}</button>` to render all the child components (`<Button>...</Button>`) returned by AddUser.js.
5. Managing the User Input State
   - in AddUser.js, create two `const [ ... ] = useState('')` for changing value states of username and age.
6. Adding Validation and Resetting Logic

   - add `setEnteredUsername('')` and `setEnteredAge('')`; add `value={setEntered...}` to the input elements; this will reset username/age to null.
   - The validation is done using this:

   ```
     if (enteredUsername.trim().length === 0 || enteredAge.trim().length === 0) {
        return
      }
      if (+enteredAge < 1) {
        return
      }
   ```

7. Adding a Users List Component
   - add **UsersList.js** and **UsersList.module.css** component under Users folder.
   - call UsersList component from App, i.e. `<UsersList users={[]} />`; notice it passes an empty array here so as to avoid the error message.
8. Managing a List of Users via State

   - to manage list of users in App.js, use `const [usersList, setUsersList] = useState([])` and add this to add user handler:

   ```
   const addUserHandler = (uName, uAge) => {
    setUsersList((prevUsersList) => {
      return [
        ...prevUsersList,
        { name: uName, age: uAge, id: Math.random().toString() },
      ]
    })
   }
   ```

9. Adding the "ErrorModal" Component
   - add **ErrorModal.js** and **ErrorModal.module.css** component under UI folder.
   - inside ErrorModal.js reuse the UI components `<Card>...<Card/>` and `<Button><Button/>` including the classes from CSS to enhance the display.
   - the ErrorModal component will be rendered in AddUser.js.
10. Managing the Error State
