[<=== Back](../README.md)

## [Related Data in Spring](https://www.baeldung.com/spring-data-rest-relationships)
*from Baeldung*

### One-to-Many Relationships

#### Data Model

In this code example, a Book is ONE *of* MANY books in a Library. Here is the creation of class Book:
```
@Entity
public class Book {

    @Id
    @GeneratedValue
    private long id;
    
    @Column(nullable=false)
    private String title;
    
    @ManyToOne
    @JoinColumn(name="library_id")
    private Library library;
    
    // standard constructor, getter, setter
}
```

Then, the relationship is added to the Library class:
```
public class Library {
 
    //...
 
    @OneToMany(mappedBy = "library")
    private List<Book> books;
 
    //...
 
}
```

#### Repository

Be sure to set up a BookRepository

`public interface BookRepository extends CrudRepository<Book, Long> { }`

#### The Association Resources

To add a Book to a Library, create a Book instance by using the `/books` collection resource. (Post your created book in Postman with a POST request).
```
curl -i -X POST -d "{\"title\":\"Book1\"}" 
  -H "Content-Type:application/json" http://localhost:8080/books
```

The response will contain the association end point.

Then, the Book must be associated with the Library by sending a PUT request to the association resource that contains the URI of the library resource
```
curl -i -X PUT -H "Content-Type:text/uri-list" 
-d "http://localhost:8080/libraries/1" http://localhost:8080/books/1/library
```

Verify the Book is in the Library with a GET:
`curl -i -X GET http://localhost:8080/libraries/1/books`

To remove an association, use the DELETE method:
`curl -i -X DELETE http://localhost:8080/books/1/library`


## [Spring Integration Testing](https://www.baeldung.com/integration-testing-in-spring)
*from Baeldung*

To utilize the Spring MVC test framework, begin by adding dependencies (found at link above)

### Test Configuration

Enable the JUnit5 extension interface **by adding the *@ExtendWith* annotation to your test classes and specifying the extension class to load*. To run the Spring test, use *SpringExtension.class***.

***@ContextConfiguration* annotation is also needed to load the context configuration and bootstrap the context that the test will use.**

```
@ExtendWith(SpringExtension.class)
@ContextConfiguration(classes = { ApplicationConfig.class })
@WebAppConfiguration
public class GreetControllerIntegrationTest {
    ....
}
```

#### The *WebApplicationContext* Object

> *WebApplicationContext* porvides a web application configuration. It loads all the application beans and controllers into the context. Now we'll be able to wire the web application context right into the test:
```
@Autowired
private WebApplicationContext webApplicationContext;
```

#### Mocking Web Context Beans

>*MockMvc* provides support for Spring MVC testing. It encapsulates all web application beans and makes them available for testing:
```
private MockMvc mockMvc;
@BeforeEach
public void setup() throws Exception {
    this.mockMvc = MockMvcBuilders.webAppContextSetup(this.webApplicationContext).build();
}
```
The *mockMVC* object is initialized in the @BeforeEach annotated method, so it doesn't have to be initialized inside every individual test

#### Verify Configuration

Verify that we're loading the *WebApplicationContext* Object properly; check that the correct *servletContext* is being attached:
```
@Test
public void givenWac_whenServletContext_thenItProvidesGreetController() {
    ServletContext servletContext = webApplicationContext.getServletContext();
    
    Assert.assertNotNull(servletContext);
    Assert.assertTrue(servletContext instanceof MockServletContext);
    Assert.assertNotNull(webApplicationContext.getBean("greetController"));
}
```

### Writing Integration Tests

#### Verify View Name

Invoke the */homePage* endpoint from our test as:
`http://localhost:8080/spring-mvc-test/` or `http://localhost:8080/spring-mvc-test/homePage`

Test code:
```
@Test
public void givenHomePageURI_whenMockMVC_thenReturnsIndexJSPViewName() {
    this.mockMvc.perform(get("/homePage")).andDo(print())
      .andExpect(view().name("index"));
}
```

#### Verify Response Body

Invoke the */greet* endpoint from our test as:
`http://localhost:8080/spring-mvc-test/greet`

Test code:
```
@Test
public void givenGreetURI_whenMockMVC_thenVerifyResponse() {
    MvcResult mvcResult = this.mockMvc.perform(get("/greet"))
      .andDo(print()).andExpect(status().isOk())
      .andExpect(jsonPath("$.message").value("Hello World!!!"))
      .andReturn();
    
    Assert.assertEquals("application/json;charset=UTF-8", 
      mvcResult.getResponse().getContentType());
}
``` 

[Baeldung](https://www.baeldung.com/integration-testing-in-spring) also contains Test examples for:
- Send GET request with Path Variable
- Send GET request with Query Paramaters
- Send POST request

### *MockMVC* Limitations

May not support all the features of a full-blown Spring application, as no real network connections are made.