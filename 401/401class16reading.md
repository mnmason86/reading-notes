[<=== Back](../README.md)

# Spring Security

## [Spring Security Architecture](https://spring.io/guides/topicals/spring-security-architecture/)

### Authentication and Access Control

Authentication: "Who are you?"
Authorization: "What are you allowed to do?"

The main strategy interface for authentication is `AuthenticationManager`, which has only one method:

```
public interface AuthenticationManager {

  Authentication authenticate(Authentication authentication)
    throws AuthenticationException;
}
```

> Spring Security provides some configuration helpers to quickly get common authentication manager features set up in your application. The most commonly used helper is the `AuthenticationManagerBuilder`:

```
@Configuration
public class ApplicationSecurity extends WebSecurityConfigurerAdapter {

   ... // web stuff here

  @Autowired
  public void initialize(AuthenticationManagerBuilder builder, DataSource dataSource) {
    builder.jdbcAuthentication().dataSource(dataSource).withUser("dave")
      .password("secret").roles("USER");
  }

}
```

## [Spring Auth Cheat Sheet](https://github.com/codefellows/seattle-java-401d2/blob/master/SpringAuthCheatSheet.md)

*Provides steps needed to use Spring Auth!*