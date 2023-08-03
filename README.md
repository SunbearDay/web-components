# js-web-components

Web components are a set of web platform API's that allow us to create custom, reusable and encapsulated HTML elements.

Web components are utilized using three technologies:

- Custom Elements - Allow us to create custom HTML elements and define their behavior.
- Shadow DOM - Allows us to encapsulate our web component in a separate DOM that is only used by our component.
- HTML Templates - These use `<template>` and `<slot>` elements to define the markup of our web component.

Basic Custom Element:

```html
<user-card name="Alice Adams">

</user-card>
```

```js
class UserCard extends HTMLElement {
    constructor() {
        super()
        this.innerHTML = `
            <h3>${this.getAttribute('name')}</h3>
        `
    }
}

window.customElements.define('user-card', UserCard)
```
