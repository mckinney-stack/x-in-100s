# 10 React Hooks - Explained

![alt text](images/{CF7D261A-749B-4791-8BD1-3376A4A594F4}.png)

React hooks use features of the React framework by calling special **hook** functions from within a component. 

We can build static - dumb - components in react by writing functions, however UI components are often dynamic. Meaning they may need to change the state of their data, react to lifecycle events, access elements from the DOM, among many other things. 

![alt text](images/{97241593-D6DA-4792-B4B9-B93377F25238}.png)

Prior to **React 16.8** developers were required to write *classes* to take advantage of certain React features.

![alt text](images/{95B4FBCD-3D3D-45DD-AC6B-238ADF0EF543}.png)

You can still use classes in React, but hooks generally provide a more ergonomic way to build components because you can reuse stateful logic without changing your component hierarchy. 

![alt text](images/{2BFCF7F0-4A7A-43CC-8C27-EE50A57A6BCB}.png)

![alt text](images/{47B4EB2E-5F74-4071-8304-5B6D57BB8687}.png)

<br>

### Several built-in hooks

React has several built-in hooks, which can be categorized into basic and additional hooks. 

![alt text](images/{B0423D78-93BE-4C95-983D-6CB16AEB728F}.png)

### Basic Hooks
1. **useState**: Allows you to add state to functional components.
2. **useEffect**: Lets you perform side effects in function components.
3. **useContext**: Provides a way to pass data through the component tree without having to pass props down manually at every level.

### Additional Hooks
4. **useReducer**: An alternative to `useState` for managing complex state logic.
5. **useCallback**: Returns a memoized callback function.
6. **useMemo**: Returns a memoized value.
7. **useRef**: Provides a way to access and persist a mutable value across renders.
8. **useImperativeHandle**: Customizes the instance value that is exposed when using `ref`.
9. **useLayoutEffect**: Similar to `useEffect`, but fires synchronously after all DOM mutations.
10. **useDebugValue**: Can be used to display a label for custom hooks in React DevTools.

These hooks cover a wide range of use cases for managing state, side effects, context, and more in React functional components. 

<br><br>

![alt text](images/{52067F36-5AF8-4F4B-B56F-C3D6D5A5E671}.png)

In the past, *stateful* logic (data that changes within the application) was tightly coupled to a class-based component.

![alt text](images/{EDB17512-96F1-41F4-9873-07CA8A016942}.png)

 This means that in order to work with reactive data, you needed to create a component. This seems reasonable, but what it led to in reality was a complex tree of nested components.

![alt text](images/{1E3136C2-D8DE-4B5E-9DFB-468325DD66F6}.png)

With this implementation, sharing any logic required some frustrating jujitsu, such as higher order components and render props, which are patterns that have you passing components as arguments to other components - which was much more complex than patterns found in Angular and other frameworks. 

![alt text](images/{DEBE259C-4D18-462D-8D4A-E7EEB7FEE4D9}.png)



<br><br>

![alt text](images/{8BC74947-9C8B-40CB-8052-EEF22BE81B59}.png)

Fortunately, hooks changed everything by giving us access to lower-level features of React outside of the context of a component. 

### Think of hooks like primitives or building blocks of the React framework

They give you special abilities that you wouldn't otherwise have with vanilla JS. 

![alt text](images/{5D680637-D90A-4537-8CC7-A712619BFD56}.png)

The hooks themselves are functions that always start with the word `use` - because you are *using* the super powers of the React framework.

![alt text](images/{3C5F52F6-60C4-4674-A57B-5B9975E9EAD2}.png)

<br><br>

### One rule to be aware of:

When using hooks you should only ever call them at the **top level** of a functional component - they don't work inside of regular JS functions (as seen below), nested functions, loops, or anything like that. 

**Exception to the rule:** when using custom hooks!

![alt text](images/{5046AA3E-4B46-4F36-A4CC-43E7C157962F}.png)

<br><br><br>


![alt text](images/{6C2CBF05-2403-473B-A94C-0E88D22B9A91}.png)

- easily the most important and often used hook
- used to handle *reactive* data
- data in the app that changes is called **"state"**
- When state changes, this should be reflected in the UI

![alt text](images/{ED527278-C818-48C0-BDE0-F869C417A4FA}.png)

- hook takes one optional argument - **the default state**
- function returns an array, containing 2 values you can use in component

![alt text](images/{8B357021-9CC2-42F8-AC78-139953F6FB9D}.png)

- returned in an array because we can destructure them with JS to easily asign the values to local vars that can be named whatever - state and setter function
- implementation of `useState` in FC's is much cleaner compared to class components, as seen below:

![alt text](images/{76F2067A-31E1-4344-91C8-0094E5EEF182}.png)



<br><br><br>

![alt text](images/{ADA8765D-2A28-4ACC-9AC6-865A6A5D39C7}.png)

- one of the most confusing hooks
- must understand the **"component lifecycle"** to understand `useEffect`
- snippet below is from a **class component**
- here we're implementing methods to *handle* different lifecycle events

![alt text](images/{5A8D7635-2DA3-40EA-8925-E1397F0BBCED}.png)

- here's a simplified version of the component lifecycle:

![alt text](images/{9B66A529-5F96-4F26-B911-42E46A40EDD0}.png)

- `componentDidMount`: component is added to the UI - or *mounted* **(can only happen once)**
- `componentDidUpdate`: reactive data on the component can change / is updated **(can happen multiple times)**
- `componentWillUnmount`: component will be removed from UI - or *unmounted* **(can only happen once)**

Keep the above *lifecycle events* in mind when talking about `useEffect` hook

<br>

- `useEffect` allows us to implement logic for each lifecycle event within a single function API
- `useEffect` takes a function that you define (as its first argument)
- React will then *run* your function - or **"side effect"** - after it has updated the DOM
- With below, it will run the function any time stateful data changes on the component
- Means it will run once when component is initialized with default value
- Then run again each time state (`count`) is updated

![alt text](images/{DC2121CD-E3CC-470A-B0E5-BA9170409A52}.png)

In most cases though, you'll likely want more fine-grained control over that behaviour. For example, imagine...

- you need to fetch data when component is initialized
- then update the state asynchronously after data's been fetched
- below would result in an infinite loop
- this is becuse each fetch updates state, which triggers re-render and another fetch etc.

![alt text](images/{7AF8B6E8-9430-413A-A8DD-A7A96BD91E84}.png)

- pass 2nd argument to `useEffect` to resolve this - array of dependencies 

![alt text](images/{2A169F0A-3477-4D95-A335-19671BC8040B}.png)

- empty array === !dependencies **(will only run once when component mounts)**
- populated array === dependencies **(will run when state changes)**

![alt text](images/{961A248B-A2D0-4B63-B670-5558905C5558}.png)

<br>

#### Teardown functions / Cleanup functions

- might want to run some "teardown" code when the component is destroyed
- implement a **teardown function** by returning a function from our `useEffect` callback

![alt text](images/{EBD42508-D3F1-4E31-9114-BF5C9ECAF2A6}.png)

- React will take the function returned, and call it when the component is destroyed


<br><br>

![alt text](images/{51F1A849-EFB4-4088-B77A-FB8BF03B9329}.png)

- `useContext` allows you to work with React's **context API**
- The Context API is a mechanism that allows you to share or scope values throughout the entire component tree

![alt text](images/{D5E4381D-A5BA-4CFB-BF53-544043357B44}.png)

- Imagine you have an object called `moods` - happy or sad
- to share current mood across multiple disconnected components, we can create a **"context"**
  
![alt text](images/{421CE16A-5E94-4FE7-9D78-CA72A1ED2C9F}.png)

- One part of the application might be "happy", so we use a context **Provider** to scope the happy mood there
- Now... any child component inside the **Provider** can inherit that value without needing to pass props down to the children 
- No need for prop drilling

![alt text](images/{C8163500-71E7-4997-B1D3-4D1117496C1B}.png)

- the `useContext` hook allows us to access - **"consume"** - the current value from the context **Provider** - even if the Provider lives many levels higher in the component tree
- reading a parent value with `useContext` is much easier than passing props down through multiple children layers - prop drilling

![alt text](images/{D398D5D9-F733-443F-AA82-C2EE131A9841}.png)

- In the above, if the mood changes from `happy` to `sad` in the parent **Provider**, the value here will be updated automatically

#### Consumer component

- the `useContext` hook is basically a much cleaner replacement for the **Consumer**


<br><br>

![alt text](images/{0A1DF2C1-09C4-439D-ADCC-10077F8281D8}.png)

- Returns a mutable object that will keep the same reference between renders
- object contains a `.current` property
- object persists for the full lifetime of a component, meaning it doesn't get reset on re-renders
- You can use `useRef` to directly access a DOM element. This is useful for tasks like focusing an input, scrolling to a particular section, or measuring the size of an element.
- Can be used when you have a value that changes, kind of like `setState`
- **The key difference:** it doesn't trigger a re-render when the value changes

![alt text](images/{AB61F1C9-502E-4016-9D4B-A3DA8C5154AB}.png)

- For example, if you built a counter button with `useRef`, we can reference the current `count` by using `count.current`
- However, when we click the button the count would never change in the UI because `useRef` doesn't trigger a re-render like `setState` does
- This can be useful when you need a **mutable** value

![alt text](images/{D28827EE-ECE6-41F2-AC09-BA3244B880F3}.png)

<br>

### Common `useRef` use case: Grabbing native HTML elements from the DOM (JSX)

- start by creating a `null` reference called `myBtn`
- connect it to raw HTML `<button>` using `ref` attribute
- can then reference the HTML button in a function to call native DOM APIs like `click()`
- this would programmatically click the button

![alt text](images/{82B06B81-5FAD-4080-9369-CCDCC7EF76E3}.png)

**The bottom line:** when you need to grab an element from the DOM, `useRef` is the hook you're looking for


<br><br>

![alt text](images/{48911970-A88C-4BA4-AE8F-7172AE7828B6}.png)

- can be quite scary
- very similar to `setState`

![alt text](images/{E2216C66-6E59-477C-BDA3-328EA880D6B0}.png)

- a different way to manage state - using **redux** pattern
- instead of updating state directly, you: 
    - *dispatch* actions that go to a `reducer` function
    - reducer function determines how to *compute* the next state

![alt text](images/{006BA12C-0BB2-4F46-85A2-FD80B4C520D4}.png)

- just like `useState`, `useReducer` returns an array of TWO values
- **first value** = reactive state you want to show in the UI 

![alt text](images/{7B892724-701A-40E2-BC11-5FC7A2DE3068}.png)

- **second value** = **where things get a bit different!**
    - instead of a function that updates the state, you're given a function that can *dispatch an action*
    - An **"action"** is just an object that has a **type**, which can be any string you want, plus an optional data **payload**

![alt text](images/{A288124C-591B-46AA-A50F-161D1B78ED35}.png)

- you might *dispatch* an action when a button's clicked, which will trigger your **`reducer`** function

![alt text](images/{9D86482B-9FBF-4214-A5CE-7F78A93D6947}.png)

- the `reducer` function is something you define
- you then pass the `reducer` function to the `useReducer` hook
- `reducer` takes the current `state` and `action` as arguments
- it uses these values to *compute* the next state
- which is usually handled inside a `switch` statement

![alt text](images/{F923F713-ED11-4C53-BFC3-31E9781ED98C}.png)

- in this case if the `action` is `"increment"` we add 1, and vice versa
- hook also takes **initial state** as its 2nd argument

![alt text](images/{EA59F96B-0418-47B5-AB4C-160BAEE3552C}.png)


### Why not just use `setState`? 

- `useReducer` helps your code manage complexity as it grows
- as you add more components to your app it becomes more difficult to manage state in a reliable and predictable way
- the **Redux** pattern can help with that
- although not everyone agrees with this

<br><br>

![alt text](images/{29C9905F-F356-40BC-B0B3-20DB2FD35B5E}.png)

- can help optimise computational cost for improved performance

![alt text](images/{A8B7B8B6-E269-42C3-A7EC-4D322DED1A76}.png)

- **Caution:** use only as needed for expensive calculations
- you don't want to prematurely optimise performance
- think of this hook as an opt-in tool to deal with expensive computations that you know are hurting performance
<br><br>
- imagine we have a function called `expensiveCount` that requires some kind of expensive computation to return a result
- instead of *re-computing* on every render, we can *memoize* the value
- we write a function that returns the computed value, then as a **2nd argument** add the dependencies to determine when this computation should be run
- in this case, whenever `count` changes

![alt text](images/{E1FD22DC-9AB2-461B-83F1-6A5675694B78}.png)

`useMemo` is great for memoizing return values, but in other cases you may want to memoize an entire function, in which case you'll want...

<br><br>

![alt text](images/{236D2474-0153-452F-AE99-B70979E3A155}.png)

- when you define a function in a component, a new function object is created each time the component is re-rendered
- usually this isn't a big deal for performance
- but in some cases, you may want to **memoize** the function

![alt text](images/{9B8E5264-9D0E-4867-BEE3-B8D6D37F8254}.png)

**Common use case:** when you pass the same function down to multiple child components

- by wrapping the function in `useCallback`, we can prevent unneccessary re-renders of the children 
- this is because they will always be using the same function object

![alt text](images/{6B3E4AA5-7C33-4B7E-85E2-54404B2FC687}.png)

<br><br><br>


![alt text](images/{A22120D4-07BE-440E-B0A5-986506FCA68C}.png)

If you build a reusable component library in React, you may need to get access to the underlying DOM element and then forward it - so it can be accessed by the consumers of your component library. 

![alt text](images/{3B9CB800-780B-4059-9AC7-BD4AF48648B6}.png)

- You can access a native DOM element with the `useRef` hook
- Then you can wrap the component in `forwardRef`
- This makes that ref available when someone uses this component
<br><br>
- `useImperativeHandle` comes in if you want to change the behaviour of the exposed ref
- you may want to modify the methods on the native element

![alt text](images/{C88FDF11-99C7-4888-870F-EF0A4A1B91A4}.png)

- In reality, the need for this hook is probably pretty rare


<br><br>

![alt text](images/{630EA951-B451-4CDD-8E5A-89C39DEF3065}.png)

- another rarely used hook
- works just like `useEffect`
- with one small difference:
    - your callback will run after rendering the component, but before painting to screen
    - means React will wait for your code to finish running before it updates the UI for the end user

![alt text](images/{E36B5F78-76C2-41E2-8CA4-902F4C4BC729}.png)

- there may be situations where you need to calculate a scroll position - or something else in the UI - before the DOM is visually updated

<br><br>

![alt text](images/{2D432042-3902-4A52-BC80-C235E8B0252D}.png)

This hook won't make sense until you start building your own custom hooks.


- If you open app in browser and open React dev tools
- You'll notice that every component in the tree will tell you a little bit about the **hooks** that are defined there

![alt text](images/{39022785-0A0A-4D10-986A-CB1EFA8AF37A}.png)

- The purpose of `useDebugValue` is to make it possible to define your own custom labels here in **React Dev Tools**
- we can build a custom hook to see that in action

### Building a custom hook:

![alt text](images/{83475D47-6711-41A5-AB37-6B908AD22874}.png)

- notice how the above component is using **two** hooks together - `useState` and `useEffect`
    - `useState` to define a display name for the user
    - `useEffect` to **fetch** that name from the database on the first render

<br>

### Define custom hook to handle this! 

- imagine we have **ten** *other* components that need to implement the *exact same logic*
- the great thing about hooks is we can easily do that by defining our own function called `useDisplayName`
- it's just a regular JS function that implements the same code we had in our component

![alt text](images/{251EFF94-6816-4373-9A8F-177D283EF4AA}.png)

- we can now put this custom hook to use in multiple components

![alt text](images/{3D49B646-7351-4898-B65B-A316CC717842}.png)

<br>

### Add `useDebugValue`

One final touch here is to add `useDebugValue` to our custom hook.

- the argument passed to `useDebugValue` will be the value shown in React dev tools

![alt text](images/{50F82870-A9FC-4E0C-B214-BE8D38BCC4E3}.png)

- As you can see below:
    - it shows the `displayName` label
    - along with the value - `"bob"`
    - as well as a breakdown of the primitive hooks that went into this custom hook

![alt text](images/{02D33D0D-6325-4524-A88E-93A03B0CC253}.png)