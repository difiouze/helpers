# Javascript DOM

#### DOM Event and Javascript loading

```javascript
document.addEventListener('DOMContentLoaded', () => console.log('Hello'))
```
---

#### Selecting Elements

##### By ID:
```javascript
document.getElementById('idName')
```

##### By Class:
```javascript
document.getElementsByClassName('className');
```

##### By Tag:
```javascript
document.getElementsByTagName('tagName');
```

##### By Selector:

###### single element
```javascript
document.querySelector('selector');
```
###### multiple element
```javascript
document.querySelectorAll('selector');
```
---
#### Creating and Appending Element

##### Creating Elements:
```javascript
document.createElement('tagName');
```
```javascript
const app = document.getElementById('app')
app.innerHTML = `<li>Hello</li>`
```

##### Appending Elements:
```javascript
parentElement.appendChild(newElement);
```
```javascript
parentElement.append(newElement);
```

##### Document fragments:
```javascript
const app = document.getElementById('app')
const data = ['Earth', 'Fire', 'Water', 'Air'];
const fragment = document.createDocumentFragment();

data.forEach(name => {
    const li = document.createElement('li');
    li.innerText = name
    fragment.append(li)
})

app.append(fragment)
```
##### Replacing DOM Elements:
```javascript
div.replaceWith(newDiv)
```

##### Cloning DOM Elements:
```javascript
originalNode.cloneNode()
```
*cloneNode(false) only clones the top elements* 
*cloneNode(true) clones all elements and subtrees* 

##### Removing DOM Elements:
```javascript
div.remove()
```
---
#### Traversing the DOM

##### Accessing Parent Element:
```javascript
const parentElement = element.parentElement;
const ancestor = element.closest(element);
```

##### Accessing Child Elements:
```javascript
const childElements = parentElement.children;
```

##### Accessing Sibling Elements:
```javascript
const nextSibling = element.nextSibling;
const previousSibling = element.previousSibling;
```

---
#### Modifying Classes

##### Adding Classes:
```javascript
element.classList.add('className');
```

##### Removing Classes:
```javascript
element.classList.remove('className');
```

##### Toggling Classes:
```javascript
element.classList.toogle('className');
```

---
#### Manipulating Attributes

##### Getting Attribute Value:
```javascript
element.getAttribute('attributeName');
```

##### Removing Attribute Value:
```javascript
element.removeAttribute('attributeName');
```

##### Check if Attribute Exists:
```javascript
element.hasAttribute('attributeName');
```

---
#### Manipulating Classes

##### Checking for Class Existence:
```javascript
if(element.classList.contains('className')) {
// Class exists
}
```

##### Replacing Classes:
```javascript
element.classList.replace('oldClass', 'newClass');
```