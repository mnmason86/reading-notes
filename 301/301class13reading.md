[<=== Back](README.md)

# More CRUD

## [CRUD Basics](https://medium.com/geekculture/crud-operations-explained-2a44096e9c88)

**Which HTTP method would you use to update a record through an API?**

PUT - this replaces all current data of the target resource with the given content

**Which REST methods require an ID parameter?**

PUT and DELETE require the ID parameter

## Speed Coding: Building a CRUD API

**What’s the relationship between REST and CRUD?**

REST controls data through HTTP commands, and CRUD is a set of functions that allow that data to be manipulated.

**If you had to describe the process of creating a RESTful API in 5 steps, what would they be?**

1. Identify what will be presented as a 'resource'
2. Decide what endpoints will be used to access resources
3. Determine how resources will be presented (json, xml)
4. Assign CRUD methods to URI's based on what the user will be doing
5. Determine any other actions that will be performed in the app (logging, security, etc.)