# React - The Complete Guide

## Section 6: Styling React Components

1. Module Introduction
   - delete the src folder from Section 5.
   - copy the new src folder from Section 6 (master)
   - run `npm install` to recreate dependencies (node_modules) folder
2. Setting Dynamic Inline Styles
   - use inline Styles within a form element with a format like this: `style={{ color: !isValid ? 'red' : 'black' }}`
   - not an effective way of dynamically changing styles; there is an better alternative
3. Setting CSS Classes Dynamically
   - a better alternative is adding CSS classes which can be dynamically appended to the `<div classname="_CSSClassName_">` using a **Template Literal**, e.g. ` <div className={``form-control ${!isValid ? 'invalid' : ''}``}> `
4. Introducing Styled Components
5. Styled Components and Dynamic Props
6. Styled Components and Media Queries
7. Using CSS Modules
8. Dynamic Styles with CSS Modules
