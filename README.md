# React - The Complete Guide

## Section 9: Diving Deeper: Working with Fragments, Portals, and "Refs"

1. Module Introduction
2. JSX Limitations and Workarounds
   - one limitation of JSX is you can't return more than one "root" JSX element; adjacent JSX elements should be wrapped by a single JSX elements, e.g. `<div>...</div>`
   - because of this single root JSX requirement, your code can easily end up with <ins>tons of unnecessary `<div>`s ("`<div>` Soup")</ins>
3. Creating a Wrapper Component
   - create a new folder called **Helpers** under components.
   - under the Helpers folder, create a new JS file called **Wrapper.js**. This file will not return JSX elements but only return **props.children** like so:
   ```
   const Wrapper = (props) => {
      return props.children
   }
   ```
   - the wrapper component is a solution to the problem (i.e. `<div>` Soup) of single root JSX requirement.
4. React Fragments
   - another workaround to JSX limitations is to use **React Fragments**. This can be implemented by using `<React.Fragment>...</React.Fragment>` or `<>...</>`.
5. Introducing React Portals
   - helps write cleaner codes.
6. Working with Portals
   - portal needs two things:
     - place you want to portal the component to
     - let the component know that it should have a portal to that place
   - <ins>public/index.html</ins> is the place to mark where the portal is, e.g.
     ```
     <body>
        <noscript>You need to enable JavaScript to run this app.</noscript>
        <div id="backdrop-root"></div>
        <div id="overlay-root"></div>
        <div id="root"></div>
        ...
     </body>
     ```
   - create two functions to portal:
     ```
     const Backdrop = (props) => {
        return <div className={classes.backdrop} onClick={props.onConfirm}></div>
     }
     ```
     and
     ```
     const ModalOverlay = (props) => {
        return (
           ...
        )
     }
     ```
   - `import ReactDOM from 'react-dom'` and use `ReactDOM.createPortal` to portal the two functions:
     ```
     const ErrorModal = (props) => {
        return (
           <React.Fragment>
              {ReactDOM.createPortal(
                 <Backdrop onConfirm={props.onConfirm} />,
                 document.getElementById('backdrop-root')
              )}
              {ReactDOM.createPortal(
                 <ModalOverlay
                    title={props.title}
                    message={props.message}
                    onConfirm={props.onConfirm}
                 />,
                 document.getElementById('overlay-root')
              )}
           </React.Fragment>
        )
     }
     ```
7. Working with "refs"

   - "refs" is short for references
   - **useRef()** are sometimes used instead of useState() during cases wherein we just want to check (and not change) the status of user inputs.
   - import `{useRef}` from react in AddUser.js; use useRef() instead of useState():
     - ```
        const AddUser = (props) => {
           const nameInputRef = useRef()
           const ageInputRef = useRef()
           ...
        }
       ```
       and use `ref=...` to connect the DOM element to the refs:
       ```
       <label htmlFor='username'>Username</label>
       <input id='username' type='text' ref={nameInputRef} />
       <label htmlFor='age'>Age (Years)</label>
       <input id='age' type='number' ref={ageInputRef} />
       ```

8. Controlled Versus Uncontrolled Components
