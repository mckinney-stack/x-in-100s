# Redux in 100s

Redux is a single source of truth for all of the data within React applications.

Redux is "framework agnostic", meaning it can be used with other frameworks than React - but React is the framework that uses it most. 

![alt text](images/{9B4A5714-1587-42DE-A07C-2495CB2C4507}.png)

Modern web applications are represented as a complex tree of components. Components that constantly produce and share data called **state**.

![alt text](images/{7E7CB72E-CBFA-4677-9284-3EC75FE7D1F0}.png)

When state is decentralized it can be difficult to understand and test. **This is where Redux comes in.**

<br>

### Redux overview

Redux is both a pattern and library that helps developers implement complex state management requirements at scale...

![alt text](images/{5D102917-EAB0-4775-90BB-4A733D2CC58F}.png)

<br>

It relies on a single immutable object to store all of the application's state - kind of like a client-side database. 

![alt text](images/{B217DD20-6BA0-4FDF-90D7-8E93BA3D633D}.png)

To change the state, such as when a button is clicked, an **action** is dispatched.

![alt text](images/{003A21C7-06C5-4B27-A9F0-73155B206914}.png)

The action has a **name** and a **payload** with the data that it wants to change. 

<br>

Remember, *the store is immutable*, so to change the state of the application an entirely new object is created by passing the current state and the action payload into a *reducer* function...

![alt text](images/{4F9F1159-2B9C-497F-84BB-A1AF4C105025}.png)

This returns a new object with the *entire application's state* - replacing the existing data in the store entirely, *instead of mutating it.*

The end result is a one-way data flow that's predictable and testable.

It also opens the door to awesome DevTools that allow you to time-travel through your application's data:

![alt text](images/{12B9564D-8552-4FA4-8763-169C7E201A53}.png)


### The downside...

It comes at the expense of additional boilerplate code that may add too much complexity to a smaller project. However, Redux Toolkit significantly reduces this boilerplate now, making it easier to manage state even in smaller projects.

<br>

### Getting started

1. Create a react app and install the redux toolkit.

Redux Toolkit is now the recommended way to write Redux logic. It simplifies many of the common tasks and reduces boilerplate. 

![alt text](images/{C8814F91-D338-44DB-AE76-5A3EA89DBF4A}.png)

1. Create the store

- use `configureStore()` to set up the global store object
- This will register any reducers to find elsewhere in the code

![alt text](images/{7CA2FF57-F46C-4020-B9B1-4758DB3D28C8}.png)

- Then `<Provider>` will make its data available to the *entire* component tree

![alt text](images/{14BAA9A4-2E4E-4C54-A8E3-80A83B5D643B}.png)

<br>

### `createSlice`

3. Define reducer logic

Next, create a "slice" to represent some data in the store.

It should have a unique name and initial state, but most importantly it contains a collection of **reducers**, which are functions that take the old state and an action, then define the logic required to change/update the state.

Redux reducers are conceptually similar to the setter functions provided by `useState`.

![alt text](images/{1147665E-4DF8-4B3D-B8E4-E3DFAD943C25}.png)

<br>

Redux toolkit will automatically generate actions that correspond to the names of these reducer functions...

![alt text](images/{69E8C26B-EA97-4DD4-8634-07C72CAF3402}.png)

We can export them, then put them to use in an actual UI component...

<br>

### `useSelector`

4. Select state

The beauty of Redux is that you can select data anywhere in your application without the need for context or prop drilling. 

Instead, you can grab any reactive value or slice within the store with the `useSelector` hook.

![alt text](images/{BCF2BF18-3D12-4CEA-9F03-349ABE1DD44E}.png)

<br>

### `useDispatch`

5. Dispatch actions

To change the application's data, an action needs to be dispatched to the store.

This can be accomplished with the `useDispatch` hook, which might send an action name and data payload on a normal browser event such as a button click.

![alt text](images/{A39A4F5F-85C3-4CBA-846F-B17C9935AEEC}.png)

![alt text](images/{D2C1D71E-034C-4921-B72E-5A200724F04C}.png)

<br>

### Redux DevTools browser extension

Serve your application and install the Redux DevTools browser extension. 

Unlike a normal project, you're able to inspect and debug the entire timeline of actions and state changes in your application. 

Redux DevTools can also be used without the extension by integrating it directly into the application code, which is useful for environments where extensions can't be installed.

![alt text](images/{90B78A09-67F6-4043-94CB-4A36EDF6CCF9}.png)

