# React - The Complete Guide

## Section 9: Diving Deeper: Working with Fragments, Portals, and "Refs"

1. Module Introduction
2. JSX Limitations and Workarounds
   - one limitation of JSX is you can't return more than one "root" JSX element; adjacent JSX elements should be wrapped by a single JSX elements, e.g. `<div>...</div>`
   - because of this single root JSX requirement, your code can easily end up with <ins>tons of unnecessary <div>s ("<div> Soup")</ins>
3. Creating a Wrapper Component
   - create a new folder called **Helpers** under components.
   - under the Helpers folder, create a new JS file called **Wrapper.js**. This file will not return JSX elements but only return **props.children** like so:
   ```
   const Wrapper = (props) => {
      return props.children
   }
   ```
   - the wrapper component is a solution to the problem (i.e. <div> Soup) of single root JSX requirement.
4. React Fragments
5. Introducing React Portals
6. Working with Portals
7. Working with "refs"
8. Controlled Versus Uncontrolled Components
