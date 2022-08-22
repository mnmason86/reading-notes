[<=== Back](/README.md)

# APIs

## [API Design Best Practices](https://docs.microsoft.com/en-us/azure/architecture/best-practices/api-design)

**What does REST stand for?**

Representational State Transfer

**REST APIs are designed around  ____**

REST API's are designed around *resources*, which are any kind of object, data, or service that can be accessed by the client.

**What is an identifier of a resource? Give an example.**

An *identifier* is a URI that uniquely identifies the resource

example: `https://adventure-works.com/orders/1`

**What are the most common HTTP verbs?**

GET, POST, PUT, PATCH, and DELETE are the most common HTTP verbs

**What should the URIs be based on?**

URI's should be based on nouns (the resource), and not verbs

**Give an example of a good URI.**

`https://adventure-works.com/orders // Good`

**What does it mean to have a ‘chatty’ web API? Is this a good or a bad thing?**

"Chatty" web API's expose a large number of resources by making many requests. This imposes a load on the server, and should be avoided when possible.

**What status code does a successful GET request return?**

200 (OK)

**What status code does an unsuccessful GET request return?**

201 (Created)

**What status code does a successful POST request return?**

201 (Created) OR if the method updates an existing resource, it returns 200 (OK) or 204 (No Content)

**What status code does a successful DELETE request return?**

204 (No Content)

#### Bookmark and Review

[RegExr](https://regexr.com/)
*pay attention to cheat sheet*
[Regex Tutorial](https://medium.com/factory-mind/regex-tutorial-a-simple-cheatsheet-by-examples-649dc1c3f285)
[Regex 101](https://regex101.com/)