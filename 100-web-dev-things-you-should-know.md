# 100 Web Dev Things You Should Know

### 1. Internet

![alt text](images/{3E3721AA-94C8-4313-802F-06CCF2BC284F}.png)

A network of billions of machines connected together. It was officially born on January 1st 1983, thanks to the establishment of...

### 2. Internet Protocol Suite

![alt text](images/{ACA769C5-F020-4BBD-93A6-5E1F8D660EF5}.png)

Internet protocol suite standardized the way these computers communicate. 

**Protocol** = a set of rules governing the exchange or transmission of data between devices.


### 3. IP address

The IP (internet protocol) is used to identify different computers on the network by assigning each one of them a unique IP address.

![alt text](images/{C8748686-CDE9-4A36-ABBB-281DB79242AE}.png)

### 4. Transmission Control Protocol

These computers can then send data back and forth with the TCP (transmission control protocol).

![alt text](images/{FD032E24-6005-4021-959A-4A68EC492CB2}.png)

### 5. Packets

![alt text](images/{D4E11179-A2C1-42D2-8CBB-260F95C78982}.png)

TCP breaks data into a bunch of small packets, kind of like the pieces of a jigsaw puzzle, then sends them through a bunch of physical components like fibre optic cables and modems, before they're put back together by the receiving computer.  

![alt text](images/{88EC34B1-6674-4281-8BC4-E257754A7F76}.png)

You can think of the internet as **hardware**, but the internet is not the same thing as the web.

![alt text](images/{272C2B48-9439-480A-809F-D2DBFA1E7787}.png)

### 6/7. Web/HTTP

The world wide web is like software that sits on top of the internet, where people can access pages with the HTTP (HyperText Transfer Protocol). 

![alt text](images/{943341D2-A400-4EF3-825D-6BC8C730BCA8}.png)

HTTP is special because it gives every page of content a...

### 8. Uniform Resource Locator - URL

![alt text](images/{57F11973-7258-4C5A-82D8-E4B75E77D80E}.png)

### 9. Browser

Humans typically use a tool called a web browser to access a URL, where it can be rendered visually on their screen.

![alt text](images/{F081609B-C705-48ED-9352-B4D3598EED79}.png)

### 10. Client

The browser is called "the client" because it's consuming information.

![alt text](images/{EA77A64C-411B-4298-B97C-E6711B12534D}.png)

### 11. Server

But on the other end of that URL, there's another computer called a "server"...

![alt text](images/{658451B3-AEDD-483E-9CCC-E6FACB706C69}.png)

### 12. Request

It received an HTTP request from the client...

![alt text](images/{88B8595A-AAC4-4DE7-9D0E-47E90618A21A}.png)

### 13. Response

...then sent an HTTP response containing the webpage content.

![alt text](images/{E4471E7E-2B13-49F7-8378-FB153F3873D8}.png)

### 14. HTTP Messages

These interactions are called HTTP messages - but more on that later. 

### 15. Domain Name

![alt text](images/{E4274318-61E9-4DEC-8DAF-0B747E9B4563}.png)

Every webpage has a unique domain name. A domain name can be registered by anyone via a registrar...

### 16/17. Registrar/ICANN

![alt text](images/{6FC45C32-7CF1-44BB-89B9-524C7D32FB46}.png)

![alt text](images/{5C1AC2AE-29F6-4799-BD97-63FC98CFD294}.png)

ICANN is a non-profit responsible for overseeing namespaces on the internet. 

### 18. Domain Name Server - DNS

![alt text](images/{772245F1-19F1-4798-8CE8-DD5603D932DF}.png)

When you navigate to a domain in a browser, it gets routed through the DNS, that maps these names to an actual IP address on a server somewhere. 

DNS is like the phonebook of the internet.

![alt text](images/{190B5F1A-EF8F-465C-98DE-4AE1054309D1}.png)

<br><br>

### 19. HyperText Markup Language - HTML

![alt text](images/{18A3CA8B-60F8-43F0-AD12-B024614338D3}.png)

When you look at a web page, the actual content you see is represented by HyperText Markup Language. 

### 20. Dev Tools

![alt text](images/{156AFBE1-0E09-4B4B-80D4-5E6990BE332A}.png)

Most browsers have dev tools, where you can inspect the structure of the HTML at any time. 

### 21. Editor

![alt text](images/{766DBEEE-215F-4EEF-9F39-CDECA1274088}.png)

To build your own web page you'll want a text editor like VS code. 

### 22. Elements

An HTML document is just a collection of elements, where an element is an opening and closing tag with some content in the middle - like a paragraph and heading. 

![alt text](images/{FECD8EB0-750E-4B25-83F9-BA4BEDFD41E0}.png)

It also has elements that handle user input, like the `<select>` and `<input>` elements, which are used to build forms. 

### 24. Attributes

In addition, elements can have one or more attributes to change their behavior. 

![alt text](images/{03F2A36D-55E5-4F98-BC65-055CC12E27F0}.png)

For example, an input can have a type like `text` or `number`, which the browser will then render differently to collect the appropriate value. 

### 25. Anchor

The element that puts the "HyperText" in HTML is the `<a></a>` anchor tag. This is a link that allows one page to navigate to a different page based on its URL.

![alt text](images/{72680CB2-6EC8-497D-96DA-466E8AE88AD1}.png)

### 26. Document Object Model - DOM

HTML elements are nested together in a hierarchy to form the "document object model" or DOM. 

![alt text](images/{0CE08E8A-F8B6-4822-B011-9D00A870EE0A}.png)

### 27. Head 

From the root element a web page is split into two parts - head and body. The head contains invisible content like metadata and a title.

![alt text](images/{D451B398-FEB4-4039-B7C8-3A1127A27A69}.png)

### 28. Body

We have the body for the main content that the end user actually sees.

![alt text](images/{5F283EC2-4AFD-4C90-BAA1-8BBE039E6498}.png)

The reason we wrap everything in tags is to give browsers and bots hints about the semantic meaning of the web page. This allows search engines to display results properly and also helps with accessibility.

![alt text](images/{445026ED-B2D3-4996-96FE-BF0541226409}.png)

### 29. Accessibility

Semantics help with accessibity for devices like screen readers that allow anybody regardless of disability to enjoy the content. 

### 30. Div

One of the most common HTML elements you'll come across is `<div>` or "division", to define a section of the web page. 

![alt text](images/{CD6C8C7A-07BF-41E5-9DB9-009AED460E58}.png)

<br><br>

### 40. CSS Box Model

![alt text](images/{736A548D-ED85-4052-B074-911C3B806027}.png)

Think of every HTML element like a box. The outside of that box is wrapped with padding, border and margin. The boxes then take up space on the page from top to bottom. 

### 41. Block

![alt text](images/{FCA96E18-69D5-492B-89D3-AE6AB62D4156}.png)

Some elements, like `<h1>` - `heading` - have a display of `block` by default, which means they take up all available horizontal space. 

### 42. Inline

![alt text](images/{99B9DAD3-BE03-442D-B34F-096FAC854D8A}.png)

Other elements, like `<img>` are displayed inline, which means they can line up horizontally side-by-side. The problem is that the default position is usually not desirable. It can be changed by customizing the position property on an element. 

### 43. Relative

![alt text](images/{DAF32B7B-8F5B-4293-BD8F-EDCF4B41BDC5}.png)

Relative positioning allows an element to move a certain number of pixels from its original position. 

### 44. Absolute

![alt text](images/{2F3D8C3F-495E-45F2-A4A2-A5BD0C34F2EB}.png)

Absolute positioning is similar but the position values are relative to its nearest ancestor. 

### 45. Fixed

![alt text](images/{15264756-EF08-475F-894D-6C298084D2A5}.png)

We then have fixed positioning, which will keep an element on the screen even as the user scrolls away from it, because it's fixed to the entire viewport. 

### 46. Responsive Layout

![alt text](images/{9E56128E-4854-4DB9-BE7F-5FC8594CF9DC}.png)

One of the biggest challenges developers face is creating responsive layouts. CSS provides a bunch of tools to help make this happen, one of which is media queries. 

### 47. Media Query

![alt text](images/{CA589270-86CA-4DD1-AFB5-4FFC0B24126D}.png)

A media query allows you to get information about the device that's rendering the web page and apply different styles accordingly.

### 48. Flexbox

![alt text](images/{01B18749-2D85-4EFC-ABBA-96622F8BF44F}.png)

CSS also provides important layout tools like flexbox. Applying `display: flex` allows the parent to control the flow of the children - to easily create rows and columns. 

### 49. Grid Layout

![alt text](images/{1D80248F-94D4-49CD-8D79-5DC7A463270B}.png)

For more complex layouts, `display: grid` can be used to display multiple rows and columns at the same time. 

<br><br>

### 50. Calc

![alt text](images/{3301463F-C752-4D1F-B417-45B0112428F6}.png)

CSS is not considered a turing-complete* programming language on its own, however, it does have *mechanisms* like `calc()` to perform mathematical operations.

    *Practically, what you need to know is that a Turing-complete language (also called a universal language) is one where you can compute anything that any other computational method can compute.

<br>

### 51. Custom Properties

![alt text](images/{BD86F621-CEAA-4CF7-926C-DEB7BCC55B14}.png)

It also has custom properties, that are like variables that you can use in multiple places. 

<br>

### 52. SASS

![alt text](images/{0FEBFDDD-36E6-416E-A022-850E794F0F6A}.png)

Vanilla CSS is rarely enough though, and many developers choose to extend it with tools like SASS, that add additional programmatic features on top of it.

<br><br>

### 53. JavaScript

![alt text](images/{5B9E430E-50AF-407B-98BE-C6CADFD4891B}.png)

Technically, you don't need JS to build a website. However, most developers choose to use it to make the user interface more interactive. 


### 54. Script Tag

![alt text](images/{D50BB4D4-4181-48BC-B42A-7F082FDE93A8}.png)

The browser interprets the HTML in your file from top to bottom, and runs the code within the `<script>` tags when it encounters it in the DOM. 



### 55. Defer

![alt text](images/{EC0B1028-4AD7-4E1D-B2B5-9AB6564BB60D}.png)

In most cases, JS is written in a separate file, then referenced as the `src` on the `<script>` tag.  

Usually, *it's preferred that this code runs after the DOM content is loaded*, which can be accomplished with the `defer` attribute. 

<br>

### 56. EcmaScript

![alt text](images/{884B79F4-E503-4226-96D5-F04D0EF70138}.png)

JavaScript is a BIG, complicated programming language, which is more formally known as **"EcmaScript"** and is standardized in all major browsers. 

![alt text](images/{48A03621-A082-4096-93E0-D153795369F2}.png)

<br>

### 59. Dynamically Typed

![alt text](images/{8B7A2AA0-EA16-409C-86A8-33374F22CFC4}.png)

JS is a *dynamically typed* language, which means no type annotations are necessary. 

<br>

### 60. TypeScript

![alt text](images/{BDDB6363-9F00-45CA-8ED7-D8E34738D5AB}.png)

That's not always ideal, so many devs choose TypeScript as an alternative, to add static typing on top of JavaScript. 

<br>

### 61. Events

One of the most common reasons you would use JS in the first place is to handle events. 

![alt text](images/{F5348672-3FE8-4A68-9BF8-2EBA0CEBE1D1}.png)

Whenever a user does something on a web page, the browser emits an event that you can listen to - like a click, mouse move, form input change and so on.

![alt text](images/{772BC556-9C5A-4D09-BFC4-FFA0E58D0ED2}.png)

<br>

### 62. Browser API 

We can tap into these events using browser APIs like **`document`**.

![alt text](images/{562970C2-AB39-4787-93C3-C9EEC89139BE}.png)

In this case, `document` provides a method called `querySelector()` that allows us to grab an element with a CSS selector. 

![alt text](images/{D408BD7C-0834-4D76-851C-8A95B7AF9A7E}.png)


### 63. Event Listener

Once we have that element set as a variable, we can then asign an event listener to it. 

![alt text](images/{310C711D-4F1E-4D1D-9C5E-9F469B1EC137}.png)

An event listener is a function that will be called, or re-executed, any time the button is clicked. 

<br>

### 66. Object

The most fundamental data structure is the object - also commonly called a "dictionary" or "hash map". 

![alt text](images/{5FC32B48-D816-481F-95A6-4FBD442A345F}.png)

### 67. Primitives

![alt text](images/{73D8D982-FFB9-410B-98A4-C1B63FB1ECDE}.png)

Anything that's **not** a primitive type, like a string or number, inherits its base functionality from the object class. 

![alt text](images/{3D863D4B-C4CE-4DD2-ADEB-C2B4B299A255}.png)

<br>

### 68. Prototypal inheritance

![alt text](images/{4BA5359D-3446-4EC8-8067-F518373A2B6F}.png)

It relies on a technique called prototypal inheritance, where an object can be cloned multiple times, to create a chain of ancestors, where the child inherits the properties and methods of its ancestors. 

### 69. Classes

This is different from class-based inheritance, which is kind of confusing, because JS also supports classes - however, these classes are just *syntactic sugar* from prototypal inheritance. 

![alt text](images/{72A0860E-2A77-4DC9-87D4-902A04AB1FE4}.png)

<br><br>

However, this is all a little too low-level. Most developers don't ever want to have to touch the word "prototype", so what we do instead is use a **frontend framework**!! 

![alt text](images/{AECD831E-4A13-41C5-B492-B330B39C5E94}.png)

<br><br>


### 70. Frontend Framework 

![alt text](images/{A83F9B2F-A1A5-45ED-87FF-2ACA7CD33E41}.png)

**Common frameworks:**

- React
- Vue
- Svelte
- Angular

All of these frameworks do the same thing in a slightly different way, which is represent the UI as a tree of components. 

<br>

### 71. Components 

![alt text](images/{FA7F87C7-9EB2-456F-9D18-58BE550E6FDE}.png)

A component can *encapsulate* HTML, CSS and JS into a format that looks like its own custom HTML element. 

![alt text](images/{FA2A1F1E-6FF0-4026-9213-6CA2BE537D6A}.png)

![alt text](images/{88ABE65C-FE95-4E40-A6CD-B627B0365EEE}.png)

<br>

### 72. Declarative code

![alt text](images/{68E20D7C-7C67-41F7-AFAA-4E23276DCE6B}.png)

Most importantly, they produce declarative code that describes exactly what the UI does. 

This is much easier to work than...

### 73. Imperative code 

...and imperative code is what you would get with just plain vanilla JS. 

![alt text](images/{55E0EBDF-9C52-4C0A-A346-E3D6B1BF7A1E}.png)

<br><br><br>


# Backend

### 74. Node.js

![alt text](images/{99DBEB78-A0D0-48F6-AF06-E97859E5B367}.png)

Node.js is a server-side **runtime** based on JavaScript.

You can run server-side code from web applications in all kinds of different languages...

![alt text](images/{C9AA60C0-2FA7-477D-8FC5-B040ADD0AFD0}.png)

...but Node is the most popular because it relies on the same language as the browser. 

![alt text](images/{177745C0-87D8-4BD7-B2FE-6BFB92CF2B3F}.png)

<br>

### 75. V8 Engine

It's also based on the same V8 Engine that powers the chromium browser...

![alt text](images/{5D605742-954C-4AA0-8F71-5C5504D95EC7}.png)



### 76. Event Loop

...to run code in a single-threaded, non-blocking event loop. 

![alt text](images/{ADD877FE-DBC2-44D6-9277-CBD64C14AA24}.png)

This allows Node to handle many simultaneous connections quickly and efficiently. 

### 77. Node Package Manager - NPM

In addition, it allows developers to share work remotely thanks to the Node Package Manager - NPM.

![alt text](images/{10BFE2DF-EDC1-4660-9718-81E7074248CC}.png)


### 78. Module

A package is also called a module, which is just a file that contains some code with an **export** statement, so it can be used in another file.

![alt text](images/{98B278B1-7CD7-4C64-88F3-600BD430E8C4}.png)

### 80. Import

The other file can consume the module by using an import statement.

![alt text](images/{0CDAAA75-7462-46D6-ADC3-FDFA0A9F2893}.png)

<br><br>

### Rendering

But now, we need to figure out how to deliver the actual website from the server to the client... 

![alt text](images/{B7D5A90D-1D3A-47BD-8D38-ADED0BB0AAE2}.png)

### 81. Server Side Rendering - SSR

The classic option is SSR. With this approach, the client will make a GET request for a certain URL.

![alt text](images/{306B7F31-B1BC-47CA-8557-DD376F746920}.png)

### 82. HTTP Method

![alt text](images/{1CEEA624-BD07-4130-BDE0-86B3371E3BBD}.png)

Every request has a HTTP Method, and GET means you want to retrieve data from a server - as opposed to methods like POST and PATCH, where the intent is to modify data. 

### 83. Status Code

![alt text](images/{0D31DC5D-1185-4682-B858-7D037FF74B6D}.png)

The server receives the GET request, then generates all of the HTML on the server (SSR) and sends it back to the client as a RESPONSE. 

The response contains a **status code**, like 200 for success, or levels 400 and 500 for errors.

![alt text](images/{CFC028B1-D22F-4513-9DF0-A03AFAA7174D}.png)

### 84. 404 Not Found

For example, if the web page doesn't exist, a server will return a 404 status code, which you've likely seen before as a web user. 

![alt text](images/{0DBB7E08-5EB9-4AC2-BAFD-4041E9533946}.png)

<br><br>

### 85. Single Page Application - SPA

**SSR** is extremely popular, but in some cases it may not be fast enough. 

Another approach is the **Single Page Application (SPA)**. With this approach, the server only renders a shell for the root URL...

    **NOTE**: CSR is the approach in which the HTML file rendering is done in the user's browser, while Single Page Application is the type of web app that incorporates this approach as its behavior. So CSR is the model under which SPAs operate.

![alt text](images/{61299005-1992-4216-9381-071016312C71}.png)

...then JavaScript handles the rendering for all other pages on the website. 

![alt text](images/{1D806298-12F1-4294-A184-2AFDFB1DB775}.png)

The HTML is generated almost entirely client-side in the browser, making the website feel more like a native iOS or Android application. 

<br>

When the app needs more data, it still makes an HTTP request, but only requests a minimal amount of data as JSON.

![alt text](images/{C751F489-6044-42EB-8371-595F5FA1D984}.png)

### 86. JSON

JSON is referred to as a "data interchange format" that can be understood by ANY programming language. 

<br>

### The problem with SPAs...

Using SPAs with CSR - built using a frontend framework like React - can result in a great user experience. However, it can be difficult for bots, like search engines and social media link previews to understand content on the page. 

![alt text](images/{0546603C-C523-4D1F-94F2-DF45D9EDBF34}.png)

This phenom lead to another rendering strategy called...

### 87. Static Site Generation - SSG

With SSG, every web page on the site is uploaded to a server in advance...

![alt text](images/{1F5D91C4-160F-4CF1-BE10-C3A92B9C1415}.png)

...allowing bots to get the information they need...

![alt text](images/{06D19A93-0AA5-4836-B293-1199EABF1642}.png)

### 88. Hydration

![alt text](images/{750F85FE-BE79-4997-B947-CC99A6F13B36}.png)

A frontend JavaScript framework usually takes over to *hydrate* the HTML, to make it fully interactive and behave like a Single Page Application. 

### 89. First Contentful Paint (FCP) & Time To Interactive (TTI)

Performance is extremely important and you'll want to use tools like lighthouse to optimise metrics like FCP and TTI.

![alt text](images/{7809F238-2BA6-47B5-B237-9E64815EA80D}.png)

### 90. Fullstack Framework

To implement one of these patterns, most developers will use a fullstack framework, like: 

- Next.js 
- Ruby on Rails
- Laravel

![alt text](images/{18AC1DB1-CF0D-4CC4-BFE2-5E57F303582E}.png)

These fullstack frameworks abstract away many of the tedious things developers don't want to have to deal with. One of which is...

### 91. Module Bundlers

![alt text](images/{A3544964-2AB0-4695-A3AD-9592091D64CB}.png)

Module bundlers are tools like **Webpack** and **Vite** that take all of your JavaScript, CSS and HTML and package it in a way that can actually work in a browser. 

![alt text](images/{B2258C0C-6BFA-4DE6-B43B-51761A9EC312}.png)

### 92. Linter

They might also provide a linter like ESlint, to warn you when your code doesn't follow the proper style guidelines. 

![alt text](images/{FDB08FE0-5989-415C-99D2-D21D26220F8A}.png)

### 93. Database

![alt text](images/{98E6F155-E1C1-451F-88EC-3682A3C98448}.png)

You will definitely need a database to build a full-stack web application, because you need somewhere to store your data, such as data about your users.

![alt text](images/{AB208561-FE8A-4B90-80A2-F673C59B5CC5}.png)

### 94. User Auth

In order to get that data, you'll need to give users a way to log in via a process called user authentication.

![alt text](images/{757948C7-F880-4DB2-8942-4E9F4347C8F8}.png)

### 95. Web Server

![alt text](images/{9348C0E7-2B7F-47C7-A795-77DBDDEC4B10}.png)

Before you deploy your code, you'll need to test it with a web server. There are tools like: 

- NGINX
- Apache

These tools allow you to create a HTTP server, BUT your framework will likely do this for you anyway, by serving the files on...

### 96. Localhost

![alt text](images/{8F1EF300-A3D6-476A-9660-39187310F56E}.png)

Localhost makes your own IP address behave like a remote web server.

### 97. Cloud

![alt text](images/{E6CE6E87-BB4E-4620-B697-73C1CEC2C56C}.png)

When it comes time to deploy, you'll likely use a big cloud provider like AWS.

### 98. Docker

![alt text](images/{950CA864-4462-4111-9CA5-62573D3AAF17}.png)

Most apps are "containerized" with docker, making them easy to scale up and down based on the amount of traffic that they receive. 

### 99. IAAS, PAAS, BAAS, SASS

![alt text](images/{C8BA7579-7B1C-4806-AFF4-D898E5D40537}.png)

There are many tools out there that function as a PAAS (Platform As A Service) to manage this infrastructure for you in exchange for your money. 

### 100. WEB3

Or if you don't want to get locked in with a giant tech corporation, you might host your application on a decentralized blockchain with Web3. 

![alt text](images/{F34F5FA0-C6DF-4F57-A6E2-957048EA8938}.png)