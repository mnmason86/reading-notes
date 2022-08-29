[<=== Back](../README.md)

# Spring MVC and Thymeleaf

> A Spring MVC is a Java framework which is used to build web applications. It follows the Model-View-Controller design pattern.
*from javatpoint.com/spring-mvc-tutorial*

## [How to Access Data from Templates](https://www.thymeleaf.org/doc/articles/springmvcaccessdata.html)
*from Thymeleaf.org*

> In a typical Spring MVC application, `@Controller` classes are responsible for preparing a model map with data and selecting a view to be rendered. This *model map* allows for the complete abstraction of the view technology and, in the case of Thymeleaf, it is transformed into a Thymeleaf context object (part of the Thymeleaf *template execution context*) that makes all the defined variables available to expressions executed in templates.

1. **Spring Model Attributes**

Add attribute to `Model` via its `addAttribute` method: 
```
 @RequestMapping(value = "message", method = RequestMethod.GET)
        public String messages(Model model) {
            model.addAttribute("messages", messageRepository.findAll());
            return "message/list";
        }
```

Return `ModelAndView with model attributes included:
```
@RequestMapping(value = "message", method = RequestMethod.GET)
        public ModelAndView messages() {
            ModelAndView mav = new ModelAndView("message/list");
            mav.addObject("messages", messageRepository.findAll());
            return mav;
        }
```

Expose common attributes via methods annotated with `@ModelAttribute`:
```
 @ModelAttribute("messages")
        public List<Message> messages() {
            return messageRepository.findAll();
        }
```

2. **Request Parameters**

Request parameters are passed from the client to server as follows:
`https://example.com/query?q=Thymeleaf+Is+Great!`

3. **Session Attributes**

```
@RequestMapping({"/"})
        String index(HttpSession session) {
            session.setAttribute("mySessionAttribute", "someValue");
            return "index";
        }
```

Session attributes can be accessed by using the `session.` prefix:
`<p th:text="${session.mySessionAttribute}" th:unless="${session == null}">[...]</p>`

4. **ServletContext Attributes**

In order to access ServletContext attributes in Thymeleaf, use the `#servletContext.` prefix:
```
 <table>
      <tr>
        <td>My context attribute</td>
        <!-- Retrieves the ServletContext attribute 'myContextAttribute' -->
        <td th:text="${#servletContext.getAttribute('myContextAttribute')}">42</td>
      </tr>
      <tr th:each="attr : ${#servletContext.getAttributeNames()}">
        <td th:text="${attr}">javax.servlet.context.tempdir</td>
        <td th:text="${#servletContext.getAttribute(attr)}">/tmp</td>
      </tr>
  </table>
```
