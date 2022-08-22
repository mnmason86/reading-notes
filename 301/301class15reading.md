[<=== Back](../README.md)

# Authentication

## [What is OAuth](https://www.csoonline.com/article/3216404/what-is-oauth-how-the-open-authorization-framework-works.html)

**What is OAuth?**

> "An open-standard authorization protocol or framework that dewsribes how unrelated servers and services can safely allow authenticated access to their assets without actually sharing the initial, related, single logon credential"

**Give an example of what using OAuth would look like.**

Using your Google login information to sign in to sites like MongoDB Atlas.

**How does OAuth work? What are the steps that it takes to authenticate the user?**

OAuth works by allowing a user to sign in to one website, and access another unrelated site or service with the same credentials, and without having to sign in a second time. 

Steps:
1. First site connects to second site using OAuth, providing the user's verified identity.
2. Second site generates a one-time token and a one-time secret unique to the transaction.
3. First site gives the token and secret to the user's client software.
4. Client's software gives the token and secret to their authorization provider.
5. Client may be asked to authenticate, then the client is asked to approve the authorization transaction.
6. User or their software approves a particular transaction type at the first site.
7. User receives an approved access token.
8. User gives approved access token to first site.
9. First site gives the access token to the second site as proof of authentication.
10. Second site lets first site access their site on behalf of the user.
11. User sees a successfully completed transaction occurring.


**What is OpenID?**

OpenID is an authentication protocol which allows users to be *authenticated* by cooperating sites using a third-party identity provider service.

## [Authorization and Authentication flows](https://auth0.com/docs/get-started/authentication-and-authorization-flow)

**What is the difference between authorization and authentication?**

Authentication verifies who a user is, while authorization is the process of verifying what they have access to.

**What is Authorization Code Flow?**

Authorization code flow exchanges an authorization code for a token on the server side of an app.

**What is Authorization Code Flow with Proof Key for Code Exchange (PKCE)?**

PKCE introduces a secrett created by the calling application that can be verified by the authorization server - called the Code Verifier. The calling app creates a transform value of the Code Verifier called the Code Challenge and sends this value over HTTPS to retrieve an authorization code. 

**What is Implicit Flow with Form Post?**

Implicit Flow with Form Post uses OpenID Connect to implement web sign-in. the web app requests and obtains tokens through the front channel, without need for secrets or extra backend calls. 

**What is Client Credentials Flow?**

With Client Credentials Flow, the system authenticates and authorizes the app rather than the user. 

**What is Device Authorization Flow?**

Device apps use the Device Authorization Flow, in which they pass along their Client ID to initiate the authorization process and get a token.

**What is Resource Owner Password Flow?**

*Not Recommended* 
Highly-trusted applications can use the Resource Owner Password Flow, which requests that users provide credentials, typically using an interactive form.

### Bookmark and Review

[Auth0 for single page apps](https://auth0.com/docs/libraries/auth0-react)