# Serverless Computing in 100s

![alt text](images/{835E14A5-2EDA-4D2C-8BF5-11AE85FDE48F}.png)

"Serverless Computing" is a misnomer used to describe servers in the cloud that require zero configuration or maintenance from the developer.

![alt text](images/{31BD73BD-3C7F-46B1-8A85-BB10D1A20625}.png)

<br>

### It's like tapping into your city's water supply

Imagine you need water for your house. You could spend a bunch of time and money digging a well, testing the water quality and plumbing it to your house...

![alt text](images/{9E5835E3-3DCA-425B-83AE-A59C165E6C2C}.png)

...OR you could just tap into the city's water supply and pay a monthly fee based on the amount of water that you use. 

![alt text](images/{DC1AF098-9BAD-4879-9CBC-91AC5FD07404}.png)


Serverless computing is *the exact same idea*, but instead of water, we're talking about... **the amount of CPU and Memory it takes to run your code!!!**

![alt text](images/{296F2299-53AB-437A-A5AF-362665C8E4A0}.png)

<br><br>

### Service Providers

Services like...

- **AWS Lambda**
- **Google cloud functions**
- **Azure functions**

...allow you to run your *back end* code across their global data centers.  

![alt text](images/{894B2963-6F98-4771-AC5A-C73168E6BFA7}.png)

Then, they mail you a bill at the end of the month that's factored down to the millisecond. 

![alt text](images/{B13BAC0E-BD80-4216-AF07-C6C23B3F8F70}.png)

<br>

### Simplifies business concerns 

With serverless computing, your only concern now is writing code.

![alt text](images/{1A7FED0B-654C-4C6D-9F24-BFA91D5C4E6E}.png)

![alt text](images/{8CA3010F-35A4-4F43-A2E0-BF5F592BB20C}.png)

You **no longer** need to: 

- Pick an operating system
- Configure networking 
- Patch dependencies 
- Provision capacity

You can now just focus on *getting rich* as the cloud handles all of the above behind the scenes! 

<br>

### Architecture

From an architectural standpoint, it allows you to develop and test each business requirement independent of a bigger, **monolithic** system. 

![alt text](images/{FEFCBEF5-9196-40C7-A5E3-FA7900179048}.png)

<br>

### Serverless Functions

Not only do serverless functions make servers easier to manage, but they can also be executed based on different events that happen in the cloud, which can actually simplify your back end code.

![alt text](images/{3F92E82F-B829-4DAF-8435-943E3CF1C8B9}.png)

For example, you might create a new database record when a user places an order, which then triggers a serverless function to send an email confirmation. 

![alt text](images/{774C9D95-4FCC-436D-9AF3-03335696F775}.png)

Or maybe an IoT event on a home security system invokes a function that sends a push notification to the user's device.   

![alt text](images/{D31AEBD4-0A89-4252-B262-8E930B166D8A}.png)

<br><br>

### Firebase Cloud Functions

One of the easiest ways to get started with serverless is Firebase cloud functions. 

![alt text](images/{5FCAD3B4-7AF0-4F79-B12B-537C04600798}.png)

The command line tool creates a project that looks like any other **Node.js** back end.

![alt text](images/{AF3B23EB-C349-4F9A-B1FC-47673240B490}.png)

In the code, we can export named functions that are configured to run on different events that happen in Google cloud.

![alt text](images/{EABE9670-BEF3-4C77-AA1B-53F59FA6E78C}.png)

An event could be a simple HTTP request, or a file upload, database write, analytics event, and so on.

![alt text](images/{8B84EDF5-B576-4EC4-9702-BCF805DB738F}.png)

After writing our code, we can then deploy it to production with a single command - `firebase deploy`. 

And we now have a reliable back end that's ready to scale! 

![alt text](images/{EC0C2E87-E611-4AEF-913B-D766AB90DE0A}.png)