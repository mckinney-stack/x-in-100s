# RESTful APIs

An Application Programming Interface (API) is a way for 2 computers to talk to eachother. 

![alt text](images/{CB5C41C2-18D6-4EA1-BC64-244225E2AB60}.png)

Using an API is just like using a website in your browser, but instead of clicking on buttons and filling out forms, you write code to explicitly request data from a server. 

![alt text](images/{184EEB04-8AB6-4FB6-AAA5-3ED842EEF5E7}.png)

For example, we could visit the NASA website to look at asteroids, OR we could use their REST API to request the raw JSON data that's shown on the screen.

![alt text](images/{C91F16B7-2543-46EB-853F-10B287357AA6}.png)

<br>

### Most APIs are RESTful

![alt text](images/{A80B44B3-A0DE-495E-B8E0-A9655A687DC5}.png)

This means they follow a set of rules or constraints known as **Representational State Transfer**.

![alt text](images/{00CEC90F-C781-4056-9053-15A04D56C307}.png)

This has been the defacto standard for API development since the early 2000s.

A **RESTful API** organises data entities - or resources - into a bunch of unique URLs*

*technically these are not URLs, but rather **URIs** - **UNIFORM RESOURCE IDENTIFIERS**.

![alt text](images/{67450EA1-3B49-468A-9670-6E3472BCD7C1}.png)

URIs differentiate different types of data resources on a server. 

![alt text](images/{9814F9E5-A99F-4789-8768-7E6FA4920FC2}.png)

A client can get data about a resource by making a request to that endpoint over HTTP.

![alt text](images/{ABF4C252-CFC6-4179-88D9-37FA47481726}.png)

<br>

### The Start Line

The request message has a very specific format. 

Most importantly, the "start line" contains the URI that you wish to access. This is preceded by a HTTP verb / request method (such as POST, PUT, GET), which signals your intent with the resource.

![alt text](images/{140B9B76-6A45-4E18-A6A3-A81A411AD2A6}.png)

- `GET` = READ
- `PUT` = CREATE
- `PATCH` = UPDATE
- `DELETE` = DESTROY

There are also a few more HTTP methods beyond the main ones outlined above. 

<br>

### Headers

Beneath the start line we have headers, which contain meta data about the request. 

The **Accept** header can tell the server you want the data in a specific format. 

The **Authorization** header can be used to tell the server that you're actually allowed to make that request. 

<br>

### The Body

![alt text](images/{2DD220B4-D8E3-4AFE-939A-406F9510092A}.png)

Beneath the headers we have the body, which contains a custom payload of data. 

The server will receive the request message, then execute some code (usually to read from a database), this is then formatted into a RESPONSE message.

![alt text](images/{03529B4C-A68A-48D7-A438-5D635C117064}.png)

The top of the message contains a status code. This tells the client what happened to their request. 

![alt text](images/{B41C3E12-F0BF-4B63-AF61-D864B317A08C}.png)

The first number in the code indicates...

![alt text](images/{12543153-7021-40C4-AA5A-80C4259A1531}.png)

We then have the response headers and body.
The headers contain info about the server and the body contains the data payload and is usually formatted in JSON. 

![alt text](images/{BDEAEB04-864C-4BEB-B6D2-F4A1809C0B25}.png)


<br>

### Stateless Architecture

An important part of this architecture is that it's stateless.

This means that the two parties do not need to store any information about each other.

Every request/response cycle is independent from all other communication.  

![alt text](images/{825B4D06-8BCE-48C4-9CC0-14F89F851281}.png)

This leads to well behaved web applications that are predictable and reliable. 