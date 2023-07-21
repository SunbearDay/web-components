# Web Components

## Basic Custom Element

```html
<user-card></user-card>
```

```js
class UserCard extends HTMLElement {
    constructor() {
        super()
        this.innerHTML = `John Doe`
    }
}

window.customElements.define('user-card', UserCard)
```

## Add an Attribute

```html
<user-card name='Alice Adams'></user-card>
```

```js
class UserCard extends HTMLElement {
    constructor() {
        super()
        this.innerHTML = `${this.getAttribute('name')}`
    }
}

window.customElements.define('user-card', UserCard)
```
