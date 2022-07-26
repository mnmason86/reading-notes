[<=== Back](README.md)

# CRUD

## Status Codes Based On REST Methods

**In your own words, describe what each group of status code represents:**

100’s = Informational codes: tell the client the server is trying to do something.
200’s = Success codes: tell client the request was accepted.
300’s = Redirection codes: tell client what they requested isn't available at that location any more.
400’s = Client error codes: tell client they are sending an incorrect request of some kind.
500’s = Server error codes: tell client the server is not functioning correctly, but may be temporary.


**What is a status code 202?**
*CREATE*

"Accepted" - Tells the client that the request was received and is being processed. Used often in asynchronous processing.

**What is a status code 308?**
*READ*

"Permanent Redirection" - Tells the client that the current url is no longer working.

**What code would you use if an update didn’t return data to a client?**

204: "No Content"

**What code would you use if a resource used to exist but no longer does?**

308: "Permanent Redirect"

**What is the ‘Forbidden’ status code?**

403 - The client doesn't have permissions to access the resource

## Build a REST API with Node.js, Express & MongoDB - Quick

**Why do we need to pull our MongoDB database string out of our server and put it into our .env?**

Because we are not going to be using local host as our server URL, and need to protect our Atlas information, which contains a password.

**What is middleware?**

Code that runs when a server gets a request, but before it is passed to routes

**What does app.use(express.json()) do?**

Allows our server to accept JSON as a body inside a post/get/etc. element.

**What does the /:id mean in a route?**

It is a parameter that we can access by using `request.params.id`

**What is the difference between PUT and PATCH?**

PATCH allows updating of individual values, whereas PUT updates all values

**How do you make a default value in a schema?**

By using `default` as the key inside the schema object.

**What does a 500 error status code mean?**

Internal Server Error - the actual server had an error, not the client

**What is the difference between a status 200 and a status 201?**

201 means 'successfully created an object', 200 means 'everything was successful', but is not specific