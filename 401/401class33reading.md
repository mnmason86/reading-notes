[<=== Back](../README.md)

**Questions**

**Describe asynchronous actions in your own words**

Asynchronous actions are actions that are performed after some other event takes place. The asynchronous method waits to execute the callback method until a response is returned.

**What is the benefit of asynchronous methods**

Asynchronous actions allow your app to run more smoothly and be more responsive. Other work can be completed while waiting on the result of a running task (in the async method)

# Amplify

## [Has Many relationship](https://docs.amplify.aws/cli/graphql/data-modeling/#has-many-relationship)
*from Amplify Docs*

> Create a one-directional one-to-many relationship between two models using the `@hasMany` directive.

```
type Post @model {
  id: ID!
  title: String!
  comments: [Comment] @hasMany
}

type Comment @model {
  id: ID!
  content: String!
}
```

> This generates queries and mutations that allow you to retrieve the related Comment records from the source Post record:

```
mutation CreatePost {
  createPost(input: {title: "Hello World!!"}) {
    title
    id
    comments {
      items {
        id
        content
      }
    }
  }
}
```

## [Completable Future](https://www.baeldung.com/java-completablefuture)
*from Baeldung*

### Asynchronous Computation in Java

> The `CompletableFuture` class implements the `Future` interface, so we can use it as a `Future` implementation, but with additional completion logic.<br><br>
For example, we can create an instance of this class with a no-arg constructor to represent some future result, hand it out to the consumers, and complete it at some time in the future using the `complete` method. The consumers may use the `get` method to block the current thread until this result is provided.<br><br>
When the computation is done, the method completes the Future by providing the result to the complete method:

```
public Future<String> calculateAsync() throws InterruptedException {
    CompletableFuture<String> completableFuture = new CompletableFuture<>();

    Executors.newCachedThreadPool().submit(() -> {
        Thread.sleep(500);
        completableFuture.complete("Hello");
        return null;
    });

    return completableFuture;
}
```

> If we already know the result of a computation, we can use the static completedFuture method with an argument that represents a result of this computation. Consequently, the get method of the Future will never block, immediately returning this result instead:

```
Future<String> completableFuture = 
  CompletableFuture.completedFuture("Hello");

// ...

String result = completableFuture.get();
assertEquals("Hello", result);
```
