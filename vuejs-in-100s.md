# Vue.js in 100s

Vue.js is a JavaScript framework for building UIs.

The creator refers to Vue.js as a "progressive framework" - meaning it can start small and scale up as large as needed.

It has the smallest learning curve compared to React and Angular. 

In vue you can start simple, and then progressively add in the tools you need to build a complex web application, such as...

- core view layer
- router
- state management
- CLI 

<br>

### Vue.js Components

At its core, it provides a way to build **components** that *encapsulate* data - **state** - in your JS, and then connect that state reactively to a template in HTML.

![alt text](images/{E46DC1FA-B8A7-4628-8D22-075342BA6A71}.png)

We call these components "declarative vues" because the same data inputs will always produce the same output in the visual UI.

<br>

### Vue.js Data

![alt text](images/{27F378FA-E9F8-4830-9400-EADDB4A2ABDE}.png)

When we declare data on this data object, it links, or *binds* it to the HTML in the template above.

When the value of the data changes, the component will automatically **rerender** - or in other words it is **reactive**.

Vue.js does a tonne of work under the hood to ensure that this process is performant across a huge component tree, using **virtual DOM**.

<br>

### Vue.js template

We can work with this data in the template thanks to Vue's HTML-based template syntax.

![alt text](images/{FCA04E5C-EC09-4143-B409-81C9C347258F}.png)

We can *interpolate* a value or expression using double curly braces `{{ likes }}`.

#### **Directives**

We also have a variety of **directives** to control the behaviour of the HTML based on the data.

For example, we can use the `v-if` directive to only render an element if the condition is **truthy**.

![alt text](images/{81FF9826-3274-42CD-921C-D2D2C6C20056}.png)

We might have a fallback element after that that's only rendered when the value is **falsy**, with `v-else`.

![alt text](images/{DF4C0117-FD4A-46B4-B881-2F983363F21A}.png)

<br>

### Vue.js declarative

We can make the app interactive by listening to events. 

Using the `v-on` directive we can listen to an event on an element, then run some code to handle that event on the right side. 

![alt text](images/{CD8DCEC2-659D-4A8D-9374-9F4B1F78196F}.png)

<br>

We can do that directly in the template, but can also define a custom method in the component's **method object**...

![alt text](images/{547656C6-F977-4645-9C0E-A0D756909535}.png)

The method has access to our reactive data and that means all we have to do is change the value of the data and the component will automatically rerender...

![alt text](images/{C37B6D69-3899-47A0-BE56-778E1F2DB521}.png)

<br>

And that is all it takes to build an *interactive, reactive, declarative* UI component with Vue. 

### Why is Vue.js loved by developers?

The framework is loved by developers for the simplicity, but also its ability to scale up in complexity incrementally.

Its plugin system allows you to easily drop in things like a **router**, **state management**, **firebase support** + more! 

![alt text](images/{2AF55F0F-76EC-44CC-A2DF-22E23771036E}.png)

<br>

And, **perhaps best of all**, it's not sponsored by some mega corporation like Google or Facebook. Therefore it's not pressured to push out new releases all the time, and does a great job listening to its community!! 

