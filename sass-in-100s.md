# Sass in 100s

Sass = Syntactically Awesome Stylesheets

Sass is a language that can *extend* your CSS - with superpowers. 

Modern UIs are extremely complex, rendering CSS hard to do. If you attempt to build a UI using plain CSS you will find that you repeat yourself often.

Sass comes to the rescue by providing a compiler that allows us to write stylesheets in a completely different language - **two** different languages to be exact.

![alt text](images/{46B949DD-3B69-4244-A19F-E427383307E8}.png)

<br>

The original indented syntax that you find in `.sass` files removes the **syntactic salt** of semicolons and curly braces `{}`, `;`.

![alt text](images/{58CEA0BB-CE75-4570-B5C8-FC3DD3FD531F}.png)

<br>

However... the *more popular* version is the superset syntax that you find in `.scss` files.   

Here you can write regular CSS, then extend it with bonus features as required! 

![alt text](images/{CB964A74-EEEB-471E-A7D7-3F81DBBA0E4F}.png)

<br>


### Variables

Sass has been around since 2006. One of its original killer features was **variables**.

Use a `$` to create a variable, then reference it somewhere else in your code: 

![alt text](images/{95FA60B0-0D0F-4D38-BDE7-87B86E65D319}.png)

Now, if that value ever changes you only have to update *one line of code*!

CSS introduced its own native variables a few years ago, but the advantages of using SASS don't end with variables! 

![alt text](images/{19B7611F-909D-47AB-AE5D-A308EE2D581F}.png)

<br>

### SASS Nesting

Killer feature number 2 is **nesting**. In many cases classes are used as namespaces, which means they're often duplicated over and over again. 

![alt text](images/{D5F3DAFD-4D68-4D39-8307-77AA549651FB}.png)

We can avoid this duplication by nesting styles inside the parent...

![alt text](images/{9FF7FDDC-4C9F-4324-B848-D2D57E39777B}.png)

<br>

By default these classes will apply to descendent elements, or they can be applied to a direct sibling by using the ampersand `&`, which itself is a tool that tells SASS to combine the parent selector with the nested child selector. 

![alt text](images/{FFAC0B25-027D-4B0C-B1D0-F267E1CA27F9}.png)

<br>

### Mixins

One other issue with vanilla CSS is that you'll find yourself using a similar group of styles over and over again on multiple different classes.

![alt text](images/{7B35F00C-4F90-4871-BEFC-18D3D7E6B7D8}.png)

Mixins allow you to encapsulate a group of styles, then apply those styles anywhere within your code using the `include` keyword.

![alt text](images/{66FDB226-EE90-4A95-8C6E-2BA300FF78C4}.png)

Mixins can also take *arguments* to create a large number of similar classes programmatically - for a group of different coloured buttons for example. 

![alt text](images/{4B45AD49-6F32-492C-AB47-985CF347B607}.png)

<br>

### Functions

In addition, Sass provides a whole suite of tools to help you write more programmatic code. 

You can use `@if` or `@else` in a mixin for more conditional logic:

![alt text](images/{C5A4E1C0-8B83-404A-AC12-5824A14E2288}.png)

<br>

### `arrays` and `@each`

You could also create an **array** of values with a variable, then loop over them with `@each`.

![alt text](images/{C4621B0F-95C2-48E7-9BE5-0A6508D84528}.png)

<br>

You may also extract all of this logic and create a **reusable function**.

![alt text](images/{6CB66B02-130C-4BDE-98E9-4756C06C22AB}.png)

<br>

OR... Sass might already have a built-in function ready to go. For example, if you need to adjust a colour based on a predictable value, you could use the built-in `lighten()` / `darken()` functions.

![alt text](images/{9D9CC3D3-0C5F-48B6-80DA-CD7ED1CE5589}.png)

<br>

When you're finished building a beautiful UI, the compiler will take you code and convert it into valid CSS that can run in the browser. 

![alt text](images/{46B949DD-3B69-4244-A19F-E427383307E8}.png)
