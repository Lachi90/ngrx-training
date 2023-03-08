<pre>
  _   _  _____ _____  __   __  _______ _____            _____ _   _ _____ _   _  _____ 
 | \ | |/ ____|  __ \ \ \ / / |__   __|  __ \     /\   |_   _| \ | |_   _| \ | |/ ____|
 |  \| | |  __| |__) | \ V /_____| |  | |__) |   /  \    | | |  \| | | | |  \| | |  __ 
 | . ` | | |_ |  _  /   > <______| |  |  _  /   / /\ \   | | | . ` | | | | . ` | | |_ |
 | |\  | |__| | | \ \  / . \     | |  | | \ \  / ____ \ _| |_| |\  |_| |_| |\  | |__| |
 |_| \_|\_____|_|  \_\/_/ \_\    |_|  |_|  \_\/_/    \_\_____|_| \_|_____|_| \_|\_____|
</pre>
# Sources
https://ngrx.io/</br>
https://www.angulararchitects.io/aktuelles/reaktives-state-management-mit-ngrx-redux/</br>
https://blog.logrocket.com/angular-state-management-made-simple-with-ngrx/

# Run
## Live Demo
<a href="https://stackblitz.com/github/Lachi90/ngrx-training/tree/main/ngrx-training" target="_blank">Run on Stackblitz.com</a>

## Locally
### First time use
`npm install`

### Run application
`ng serve`

# Know How
## State Management Lifecycle
<img src="./readme/ngrx-state-management-lifecycle.drawio.png">

## General Explanation
### Actions
> Actions are events which are triggered throughout the appliction. This could be user interactions or network requests.

### Reducers
> Reducers are responsible to transition the state from one to the next. Reducers have functions which are trigger on base of the action's type.

### Selectors
> Selectors are pure functions used for obtaining slices of store state.

# Development Parts
## Packages added
- @ngrx/store@14.0.2

## Actions
### Book Action
The `books.actions.ts` defines two [action groups](#action-group). The first for adding and removing books and the second one for the book API.</br>
`source` is the group name.</br>
`events` represents a list of actions. The key is the action name.</br>
The `props` method is used to define any additional metadata needed for the handling of the action.

## Reducer
- Book Reducer
- Collection Reducer

### Reducers explained
The two reducers work by the same principle. The `createReducer` function retrieves the initial state as there first parameter. 
Every other parameter are action handlers, they are represented by the `on` function. As first paramter the action name is passed (which is part of the actions ts file). The second paramater handles the state transition. 

## Selector
- Book Selector

## Services
- Books Service

## Components
- BookList Component
- BookCollection Component

# Glossary
## Action Group
An action group is used to group various actions with the same source.