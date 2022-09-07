[<=== Back](../README.md)

# Spring Boot and OAuth2

#### Steps to write a Client Application
With access token from GitHub

- In the project, create a homepage at index.html with linked stylesheet

- Secure the application with GitHub and SpringSecurity
```
<dependency>
	<groupId>org.springframework.boot</groupId>
	<artifactId>spring-boot-starter-oauth2-client</artifactId>
</dependency>
```

- Add a new GitHub app
  - Settings > Developer settings > OAuth Apps > Register a new application
  - Authorization callback URL -> `http://localhost:8080/login/oauth2/code/github`

- Configure application.yml
```
spring:
  security:
    oauth2:
      client:
        registration:
          github:
            clientId: github-client-id
            clientSecret: github-client-secret
```

- Run your app and visit the home page at `http://localhost:8080`

#### What Just Happened?

> The app you just wrote, in OAuth 2.0 terms, is a Client Application, and it uses the authorization code grant to obtain an access token from GitHub (the Authorization Server).

It then uses the access token to ask GitHub for some personal details (only what you permitted it to do), including your login ID and your name. In this phase, GitHub is acting as a Resource Server, decoding the token that you send and checking if it gives the app permission to access the user’s details. If that process is successful, the app inserts the user details into the Spring Security context so that you are authenticated.
