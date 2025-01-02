# Angular in 100s

Angular is a TypeScript framework for building UIs.

It was built by **Google** and released in 2016 as the sequel to **Angular JS**. 

To get started, use its hugely powerful CLI tool to generate your initial application.

![alt text](images/{299C28BD-4AA5-4521-AD05-463DEF0BB0C5}.png)

When you do this, your app comes preconfigured with:

- routing
- a testing framework
- your fav style preprocessor

In addition, the `ng add` command can turn your app into a PWA (progressive web application), add SSR (server side rendering) and provide Firebase support!. 

![alt text](images/{22BF4E1E-9672-45FD-A746-834FE1710067}.png)

![alt text](images/{04C45374-5994-4F3B-8D91-82A3642C2F86}.png)

![alt text](images/{19C59789-8D8E-476D-8A94-1013E0E3B028}.png)

<br>

### Components

At its core, Angular is just a component-based UI library.

You can create a component with the CLI...

![alt text](images/{C37307E2-BE0B-4F9F-ADBA-DA90F893654E}.png)

If you then navigate to its TS file, you notice the component *decorator* - `@Component` - which makes this TypeScript class a component. 

Any properties on this class are considered reactive state, and when their values change the component will rerender the UI. 

![alt text](images/{E7655A2E-3C92-487B-80D8-42EB30338380}.png)

<br>

For example, we can bind the property to HTML using double curly braces `{{ }}` in the template.

![alt text](images/{A89EE08C-C373-4E39-8624-64DE8F583F65}.png)

<br>

From there, we could add a button that increments the value each time the button's clicked. 

![alt text](images/{0FDA7786-3784-4A96-8410-D300BC45839A}.png)

We add the event name on the left side and an expression on the right. This points to a method in our class. 

Each time the button is clicked, it calls the method, which changes the state, which triggers a rerender in the UI. 

<br><br>

Angular also has a variety of directives for building complex templates. 

You can use `ngIf` to handle conditional logic.

![alt text](images/{2BD262C1-E4F5-4167-B36C-CDF698C788EF}.png)

<br>

If you have an iterable value, use `ngFor` to loop over it. 

![alt text](images/{123FEA80-3878-4773-A2B2-DB630CDDB08B}.png)

<br>

### Service

Where angular really excels is handling complexity, and one of its primary tools for doing so is called "Dependency injection". 

When your app grows to hundreds of components, you'll likely need a way to share data and functionality between them. 

We can take our component logic here and extract it into a service, which can be treated as a global singleton throughout the application. 

![alt text](images/{00AE5C99-A50B-4C59-B5B9-77A6C998E9CF}.png)

Now, any component that wants to use this state or logic, can simply add this class to its constructor. 

![alt text](images/{D1A0159C-4A3C-4FFF-AC09-BFE4C7F5DCFB}.png)

The end result is a simple and reliable way to compose comlex applications.

As a developer, you can always count on a consistent experience between projects - and minimal decision fatigue.