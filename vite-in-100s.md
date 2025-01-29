# Vite in 100s

Vite is a JS build tool that simplifies the way we build and develop frontend web applications. 

At its core it does two things: 

1) Serve your code locally during development

![alt text](images/{0BC42FD4-476E-4784-A2AA-1BA34A89FAE2}.png)


2) Bundle your CSS, JS and other assets together for development

![alt text](images/{01E0C795-DB45-44E1-9759-49F48B1BE93A}.png)

<br>

### One of many similar tools

There are many tools out there that do the same thing - like Webpack - so what makes Vite different? 

![alt text](images/{93F3F1AA-AEF8-4C64-B716-2D87768DCC21}.png)

It was created by Evan You in 2021, who also created **Vue.js**, as a way to both simplify and speed up the build process.

![alt text](images/{4B733AE5-2112-45B2-86E9-D13A7C423E6E}.png)

<br>

Not long ago, developers had no native way to combine JS files together in a modular way. 

![alt text](images/{856F1758-C4E7-479B-ABBD-AD968B703645}.png)

This led to JS bundlers like **Webpack** and **Rollup** that concatenate multiple files together into a single bundle for the browser. The problem is that this process becomes increasingly slow as the app adds more code and dependencies. 

![alt text](images/{5F80B54D-C7DE-4F27-8004-BE2F849BAECD}.png)

<br><br>

![alt text](images/{C91A81A9-30BB-4B03-AC71-BA828A11D8E0}.png)

In 2015, EcmaScript (ES) Modules were introduced and by 2020 they had wide browser support... 

![alt text](images/{40B70063-3FC3-42AF-AD74-0D33FF13E8D0}.png)

...allowing developers to import and export code from different files in the browser. 

**Vite** leverages native ES modules in the browser to load your code instantly, no matter how large the app is. 

![alt text](images/{56AE0E65-3398-492D-AD7C-344A500B3507}.png)

![alt text](images/{8B9AAEC2-4D04-411B-9DB9-107B88DD8892}.png)

It also supports **Hot Module Replacement** for an extremely fast feedback loop during development. 

<br>

### Uses Rollup under the hood when building for production

![alt text](images/{36229C83-DB9A-45CE-9DC5-76E782C94D68}.png)

When building for production, Vite uses Rollup under the hood, so you don't have to worry about configuring it. 

### An opinionated tool!

![alt text](images/{4C40D5BB-C9DE-42D3-A703-F8E1DD5E9E6E}.png)

Vite provides conventions that work out of the box for most developers.

<br>

### Getting Started

Run `npm init vite` from the command line. 

![alt text](images/{A84D2F7B-84AE-4897-96A8-15452B17EA20}.png)

Then choose a starter project with your favourite frontend framework.

You'll notice the project comes with a **vite.config.ts** file.

![alt text](images/{984ACE6C-C2EC-4082-AFFE-2B8FEBEEAEB5}.png)

It has a plugin ecosystem that can extend it with additional features, and you can also manually override the Rollup defaults when neccessary. 

![alt text](images/{10861AF3-54AB-4877-9A1A-1D5AECE113EB}.png)

There are some really cool plugins out there, like Vite SSR, that can do SSR like **Next.js**.  

<br><br>

To serve the application locally, run `npm run dev`. 

![alt text](images/{2F56D2A6-E837-48FC-B6FB-42DC3CA3C31F}.png)

<br><br>

Even if you install a bunch of big dependencies like **Lodash** and **Moment**, the time to run the dev server does not change. 

![alt text](images/{3170C2E6-E4AB-406C-8B6A-15DDCA34B52F}.png)

If you open the **Network** tab in the browser's dev tools panel, you'll notice that instead of importing a single JS bundle file, it's importing our actual source code - like a raw tsx file in this case.

![alt text](images/{F474B2CF-BEA7-44E8-87FD-2E676DBF5AD8}.png)

<br>

### Makes TypeScript 20/30x Faster

![alt text](images/{35FF2D63-9059-4FDA-8914-EBF56042BFCB}.png)

This is because it skips type checking and uses ES Build to transpile your code. 

<br><br>



As you're developing your app, you might change the state of it in the UI then realise that some of the code needs to change...

![alt text](images/{118526ED-8082-4F02-A480-8005164D4CE0}.png)

...when you modify the source code, the changes will be reflected instantly without losing that state of the application... 

![alt text](images/{C17DBDB5-B5DE-4766-8F27-3EC3C98FBBAB}.png)

That's what we call **Hot Module Replacement (HMR)!!**

![alt text](images/{A925266F-204F-4F02-80C2-3DAC34887130}.png)

<br><br>

Now, run `npm run build` to build the app for production. 

![alt text](images/{9E1EB44B-DE13-4D11-96A1-F0C47977D749}.png)

This will generate a JS bundle with Rollup, with a bunch of automatic optimizations, like automatic code-splitting, for any dynamic imports and CSS. 

![alt text](images/{4966B9F8-53E5-4B8E-BE44-CC5625CEB8DF}.png)