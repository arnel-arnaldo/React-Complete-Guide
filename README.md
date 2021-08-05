# React - The Complete Guide

## Section 7: Debugging React Apps

1. Module Introduction
   - this is a section about finding & fixing errors
   - the example files (from Section 6) are slighly altered so there will be errors when run.
   - delete the src folder from Section 6.
   - delete the package.json and package-lock.json.
   - copy the new src folder from Section 7 (master).
   - copy the new package.json from Section 7 (master).
   - run npm install to recreate dependencies (node_modules) folder.
2. Understanding React Error Messages
   - a message can imply the error be of the two types: **typo or syntax error**.
3. Analyzing Code Flow and Warnings
   - there's another error that doesn't display messages but output is wrong: **logic error**
   - you can use your browser **Dev Tools (F12)** to see if there's any warning that might implicitly be related to the logic error.
4. Working with Breakpoints
   - on your <ins>Dev Tools > Sources<ins>, locate the file you want to debug. Then you can click on the line number where you wish to have the breakpoint. The execution will pause on the breakpoint and then you can execute each line step-by-step from there. From there, you can check the values of variable.
5. Using the React DevTools
   - add the **React Developer Tools** to your browser.
