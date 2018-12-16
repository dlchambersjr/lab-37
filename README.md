# Lab-37: Login/Auth

## Author: David Chambers

## Links and Resources
* [repo](https://github.com/dlchambersjr/lab-37)
* [sandbox](https://codesandbox.io/s/oloy29z16q)

### Modules

#### `index.js` -> renders to the DOM
* Purpose: Wraps the module(s) to be rendered in the store provider.
* Renders `<App/>`

#### `store/index.js`
##### Exported Values and Methods

###### `store() -> reducers and middleware`
* Records: state created by the records reducer
* Thunk: middleware to assit with Async processes.

#### `App.js` -> renders `<LoginContext>, <Login>, and <Auth>` to index.js
##### Exported Values and Methods


#### `components/record/list.js` -> player list and `<Record>`
##### Exported Values and Methods

###### `deleteRecord` -> object for `handleDelete()`
Creates the necessary information to be passed to the reducers to delete a specifc record.

###### `editRecord` -> updates state
Updates state with the id of the record selected to edit and displays the form with that record.

###### `reset` -> updates state
Updates state with a **null** id to clear the form.

###### `componentDidMount()` -> list of records
Retrieves a list of records from the chosen model.

#### `components/record/record.js` -> form based on model schema
##### Exported Values and Methods

###### `componentDidMount()` -> schema for form generation
Retrieves the schema from the chosen model and provides it to the Redux form generator.

###### `resetPlayer` -> updates state
Updates state with a **null** id to clear the form.

###### `handleSubmit` -> object from form data
Collects the data from the form and compiles it into an object for the reducer.

#### `components/record/actions.js` -> requested data based on action
##### Exported Values and Methods

###### `post` -> object with post data
Prepares information for the reducer

###### `runPost` -> object for reducer

###### `get` -> object with get data
Prepares information for the reducer

###### `runGet` -> object for reducer

###### `put` -> object with put data
Prepares information for the reducer

###### `runPut` -> object for reducer

###### `destroy` -> object with destroy data
Prepares information for the reducer

###### `runDestroy` -> object for reducer


#### `components/record/reducers.js` -> updates state
##### Exported Values and Methods

###### `GET` -> updates state
Retrieves information defined in `actions.js` and updates state.

###### `POST` -> updates state
Saves information defined in `actions.js` and updates state.

###### `DELETE` -> updates state
Removes information defined in `actions.js` and updates state.

###### `PUT` -> updates state
Replaces information defined in `actions.js` and updates state.

###### `PATCH` -> updates state
Updates information defined in `actions.js` and updates state.


#### `components/lib/api.js` -> schema data
##### Exported Values and Methods

###### `get(url)` -> schema
Retrieves the data from the passed url.

#### `components/if/if.js` -> boolean
##### Exported Values and Methods
Used to return a boolean that is used to decide whether to display a sectgion or not.

#### `components/auth/context.js` -> login state
##### Exported Values and Methods
Used to maintain the state of the login and pass it to other components.

###### `login` -> cookie and updated state
Upon successful authorization, a cookie is stored and the login status is updated in state.

###### `logout` -> updated state
Upon logout the authorization cookie is removed and the login status is updated in state.

#### `components/auth/auth.js` -> renders children
##### Exported Values and Methods
Used as a wrapper to render children based on role.

#### `components/auth/login.js` -> form data
##### Exported Values and Methods

###### `handleSubmit` -> token
Returns a token based on the login credientials submitted

###### `handleChange` -> updates form
Updates the form in place as input occurs

## Setup
### `.env` requirements
* `PORT` - Port Number
* `MONGODB_URI` - URL to the running mongo instance/db

### Running the app
* `npm start`

### Tests
* I will need to test the DOM changes and state changes in the various modules.

### UML
[login-auth-uml](https://raw.githubusercontent.com/dlchambersjr/lab-37/master/lab37-login-auth-uml.jpg)
