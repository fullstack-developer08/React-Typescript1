# React with Typescript Part 1 with classnames

## Prerequisite:

We should know how to create react project with create-react-app

The same way we used to create the project for react+typescript

## Installation:

```sh
npm install -g create-react-app

create-react-app my-app --scripts-version=react-scripts-ts

cd my-app/

npm start
```

## Removing default feature of tslint from tslint.json file

### 1. strict import orders

Default tslint setting is all import should be start in alphabetical order.
to remove default setting we need to change rule in tslint.json file

```javascript
"rules": {
    "ordered-imports": false,
}
```

### 2. strict key orders

When we assigning the key and value to any variable default is required 
in alphabetical order but I don't want this default setting so for that we can use
below rule.

```javascript
"rules": {
    "object-literal-sort-keys": false
}
```

### 3. restrict of console.log
    The project will not allow you to put console.log so to stop this default feature
we need to use below tslint rule property

```javascript
"rules": {
    "no-console": false
}
```

## classnames (Using this module to make className as conditional bases)

```sh
npm install --save classnames
npm install --save-dev @types/classnames
```

```javascript
import * as classNames from 'classnames';

const navbarClass = classNames({
      navbar: true,
      'is-info': !this.state.navIsLink,
      'is-success': this.state.navIsLink,
});

<nav className={navbarClass}>
```