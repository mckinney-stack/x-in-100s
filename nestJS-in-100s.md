# Nest.js in 100 Seconds

**NestJS** is a **Node.js** framework for building scalable, server-side applications with TypeScript. 

![alt text](images/{7953A145-C8D8-4887-8F1C-B920B8DFE875}.png)

It provides a suite of tools that leverage either **Fastify** or **Express** to facilitate rapid development and predictable, readable code. 

![alt text](images/{81B82508-AD77-4C6C-926F-ABAC2B00EA2F}.png)

It supports **REST** and **GraphQL** APIs out of the box.

![alt text](images/{51A3BBE4-2423-4677-9C15-BDA08C9FC761}.png)

Or, you might use it to build a full-stack application using the model view controller pattern - similar to frameworks like **Laravel** or **Ruby on Rails**.

![alt text](images/{293EEB21-5EC3-4009-87AA-1955212E302B}.png)

NestJS contains a bunch of built-in modules to work with databases, handle security, implement streaming and anything else you can imagine doing in a server-side application...

![alt text](images/{31BFEA9A-A36B-4E7A-8BE9-101530A80069}.png)

![alt text](images/{E9BB45E5-F59F-4276-A762-C25BFF69495A}.png)

![alt text](images/{A4AD2D28-7F61-48C5-B832-BE7A4BB28591}.png)

![alt text](images/{C834E67B-B629-4D04-AEA7-11EBD54FBBEA}.png)

![alt text](images/{37BC5D7D-C823-4871-99AC-04E4AC83E4FD}.png)

<br><br>

### Powerful CLI

Nest has its very own powerful command line tool. 

You can scaffold out a new project with the `nest new` command.

![alt text](images/{42BE993C-4DBC-4113-B393-146987097F58}.png)

This command provides a codebase pre-configured with **Jest** for testing, and set up with **TS** to help us create more readable and reliable code.

![alt text](images/{6946A199-62FF-4C35-872B-2B3C61C1E8B4}.png)

<br>

### Controller

In the `src` directory, you'll notice a "controller", which is a fundamental building block of the framework.

![alt text](images/{919FF6C6-31BB-4456-B244-09ED4D9F4EF4}.png)

It's responsible for **handling incoming HTTP requests** and **returning responses back to the client.** 

![alt text](images/{99043529-22D7-41BB-98BB-76A4C8A17094}.png)

To implement a controller, simply add the `@Controller` decorator to a class. Then, inside the class, you can implement methods and decorate them with **HTTP verbs** like: 

- `@Get`
- `@Put`
- `@Post`
- `@Patch`

<br>

![alt text](images/{1AD8EB63-E330-4886-BD9A-38DCBED48895}.png)

By default, this will create a HTTP endpoint on the root URL, but you can also pass a **string** to the decorator to change the route, or implement dynamic route parameters:

![alt text](images/{315D205D-4B57-45EE-A7F2-88324F281B2A}.png)

In addition, nestJS provides other decorators to control things like the **status code** and **headers**:

![alt text](images/{B5691B8E-122B-4B31-8287-2AD422EC3368}.png)

![alt text](images/{DD35030C-00B7-48A0-B5A0-265BF2C01AD7}.png)

Then in the method itself, parameter decorators can be used to access the **request** parameters or body:

![alt text](images/{84325023-7BCD-42A8-8FDC-4DB7F0DBB089}.png)

Finally, the return value from the method is the response **body** that gets sent back down to the client:

![alt text](images/{F8988B0E-8646-48EE-B077-42BF4459B0CB}.png)

<br><br>

### Generate more controllers with the CLI

What's awesome about nest is that you can use the CLI to automatically generate more controllers - to keep your code organized as it grows in complexity. 

![alt text](images/{64FE63B5-527D-4349-8507-A76EB085DFD7}.png)

<br><br>

### NestJS Providers

There's more to Nest than just controllers. A *provider* is `class` that contains shared logic throughout the entire application - and can be injected as a dependency where needed.

![alt text](images/{311AC52B-DD6B-4EA8-867D-EE844C68F107}.png)

Any class with the `@injectable` decorator can be injected in the constructor of another class.

![alt text](images/{2B2630A7-8ED9-4052-B3B0-489A58940A01}.png)

For example, a provider can be implemented as a guard to handle role-based user authentication. 

![alt text](images/{E1EFD399-8C55-4153-8957-F29475C4BDCC}.png)

Or, it might be implemented as a pipe to efficiently validate and transform values in a controller. 

![alt text](images/{0800C1A2-EC1B-4C90-936D-26478D354831}.png)

<br><br>

### The `@Module` decorator

Lastly, we have the `@Module` decorator, which allows code to be organized into smaller chunks, where it can be lazy-loaded to run faster in serverless environments.

![alt text](images/{6900F75C-34CE-47F5-AE33-52D870B51271}.png)

