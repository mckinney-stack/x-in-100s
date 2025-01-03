# Tailwind in 100s

Tailwind is a massive collection of tiny CSS utility classes for quickly and consistently building good looking websites.

CSS and design are hard. But naming your CSS classes in a sane way is virtually impossible. 

![alt text](images/{7E1CF0C0-11D6-49E2-8ACB-2A0FF785779E}.png)

<br>

Frameworks like Bootstrap and Material address this problem by creating styles for **high-level components** - things like buttons, dropdowns and forms. 

![alt text](images/{1A18CA06-3B56-45C6-834E-CAA05544795A}.png)

<br>

Tailwind takes a more *functional* approach, by providing you with utility classes that can be composed together to build components like this:

![alt text](images/{4FECF3AF-4488-468E-A3DF-64A442E719BD}.png)


Instead of using the "card" class like you might in Bootstrap, you combine utility classes such as:

- `flex` == display: flex;
- `p-4` == padding: 1rem;
- `m-1` == margin: .25rem;
- `bg-green-50` == background-color: rgba(236, 123, 131);

<br>

### Conditional Styles

In addition, every utility can be applied conditionally. 

You have variants like small, medium and large for responsive designs...  

![alt text](images/{6D1B038C-749B-4B02-A95F-BB7D45BB88C8}.png)

...along with a bunch of pseudo selectors like `hover:` and `focus:` to handle state changes.  

![alt text](images/{213AB358-BA30-4B61-94F1-ACEBBDB220BC}.png)

You also have `dark:` which renders different colors when dark mode is enabled.

![alt text](images/{717E9901-5B5D-4151-88B3-F571552946C7}.png)

<br>

This approach gives you a lot more freedom over your creativity when compared to other CSS frameworks. 

![alt text](images/{40E96BA9-5BA7-42B3-A423-611DC4A50FFA}.png)

<br>

### Design System

At the same time, using Tailwind provides a design system out of the box, which you don't get with plain CSS.

![alt text](images/{2D09A5B8-FEDC-47C4-8FC5-4572F8ABBAFF}.png)

It lives in the sweet spot between convention and configuration

![alt text](images/{24675E53-D9BB-43C2-AB0D-F83FD115C60B}.png)

<br>

### Ugly HTML

The flipside is that it does create some ugly HTML - this is the big trade off!

![alt text](images/{C2DC30DE-EB26-4DF8-8860-483ED7DE9ABF}.png)

You have tonnes of hard to read, duplicate class names - as your UI grows *duplication will happen*!! 

<br>

You can avoid this by creating reusable components with a modern front-end JS framework! 

![alt text](images/{478A006D-DE24-496E-A54D-AEA522039A1E}.png)

OR... by using the `@apply` directive in CSS to take tailwind classes and compose them into a single, concise class name. 

![alt text](images/{B80D56B8-C96F-40B0-8859-087F65F3F10F}.png)

<br>

### Performance Concerns

Tailwind weighs in at 3,566kbs during development, but when you go to build for production, it will automatically purge any unused utility from the final bundle, resulting in minimal dead code, and thus faster page loads.

![alt text](images/{466971E4-394E-41C0-89D5-E583E5492955}.png)

<br>

### Awesome Tooling! 

Where tailwind really shines is with its tooling. You don't need to memorize much because VS code will autocomplete every tailwind class for you. 

AND if you're not sure what it does, just hover over it and it will show you the equivalent code in plain CSS.

![alt text](images/{35DA601F-0302-496A-9BEB-0FE851F6B293}.png)

If you're not happy with what it does, you can easily customize everything from the colour palette, to the spacing, to build your own unique design system. 
