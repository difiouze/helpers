# Frontend Interview

#### HOW THE `this` KEYWORD WORKS

👉 **this keyword/variable**: Special variable that is created for every execution context (every function).  
- Takes the value of (points to) the "owner" of the function in which the `this` keyword is used.

☝️ **this is NOT static**. It depends on **how** the function is called, and its value is only assigned when the function is actually called.


##### Method  
👉 `this = <Object that is calling the method>`

🔒 In strict mode! Otherwise: `window` (in the browser)


##### Simple function call  
❌ `this = undefined`


##### Arrow functions  
🎯 `this = <this of surrounding function (lexical this)>`



##### Event listener  
🎧 `this = <DOM element that the handler is attached to>`


```javascript
const jonas = {
  name: 'Jonas',
  year: 1989,
  calcAge: function() {
    return 2037 - this.year;
  }
};
jonas.calcAge();  // 48

```
👉 **calcAge** is a method  
👉 **jonas** refers to the object  
👉 **1989** refers to the year

👍 **Way better than using** `jonas.year!`

☝️ **this** does **NOT** point to the function itself, and also **NOT** to its variable environment!

---

#### `var` vs `let` vs `const`


- **var**
  - Function scoped
  - Hoisted - initialized as `undefined`

- **let**
  - Block scoped
  - Reference error if accessing before declaration

- **const**
  - Block scoped
  - Reference error if accessing before declaration
  - Must be initialized on declaration and cannot be re-assigned a new value


##### When to use each one of them?

- Always use **const** declarations.
- If the value is expected to change, use a **let** declaration.
- **var** declarations can be avoided as they introduce unintended behavior.

---