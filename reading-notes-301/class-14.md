# Notes - Day 14

_<a href = "https://www.csoonline.com/article/3216404/what-is-oauth-how-the-open-authorization-framework-works.html">"What is OAuth"</a>_

1. What is OAuth? An open-standard authorization protocol or framework that describes how unrelated servers and services can safely authenticate access to their assets without actually sharing initial, related, single logon credential.

2. Give an example of what using OAuth would look like. When you go to log onto a website and it offers to log on using another website’s/service’s logon. You then click on the button linked to the other website, the other website authenticates you, and the website you were originally connecting to logs you on itself afterward using permissions gained from the second website.

3. How does OAuth work? OAuth essentially allows the user, via an authentication provider that they have previously successfully authenticated with, to give another website/service a limited access authentication token for authorization to additional resources.

- What are the steps that it takes to authenticate the user? Website A connects to the website B on behalf of the user, using OAuth, providing the user’s verified identity. Website B generates a one-time token and a one-time secret unique to the transaction and parties involved. Website A gives this token and secret to the initiating user’s client software. Client’s software presents the request token and secret to their authorization provider. If not already authenticated to the authorization provider, the client may be asked to authenticate. After authentication, the client is asked to approve the authorization transaction to the website B. The user approves (or software silently approves) a particular transaction type at website A. User is given an approved access token. The user gives the approved access token to website A. Website A gives the access token to website B as proof of authentication on behalf of user. Website B lets website A access their site on behalf of the user.

4. What is OpenID?  OpenID is about authentication. "penID is for humans logging into machines, OAuth is for machines logging into machines on behalf of humans." . In 2014, OpenID Connect was released, which reinvented OpenID as an authentication layer for OAuth.

Security Assertion Markup Language, or SAML. Refers to an XML variant language, SAML describes a framework that allows one computer to perform both authentication and authorization on behalf of one or more other computers, unlike OAuth, which requires an additional layer like OpenID Connect to perform authentication.

OAuth Version 2.0 creators focused on making OAuth more interoperable and flexible between sites and devices

_<a href = "https://auth0.com/docs/authorization/flows">"Authorization and Authentication flows"</a>_

1. What is the difference between authorization and authentication? authentication is the process of verifying who a user is, while authorization is the process of verifying what they have access to.

2. What is Authorization Code Flow? Exchange of a Authorization Code for a token. Your app must be server-side because during this exchange, you must also pass along your application's Client Secret, which must always be kept secure, and you will have to store it in your client.

3. What is Authorization Code Flow with Proof Key for Code Exchange (PKCE)? It introduces a secret created by the calling application that can be verified by the authorization server; this secret is called the Code Verifier. Additionally, the calling app creates a transform value of the Code Verifier called the Code Challenge and sends this value over HTTPS to retrieve an Authorization Code

4. What is Implicit Flow with Form Post? You obtain an ID token using authorization code flow performed by the app backend.

5. What is Client Credentials Flow? System authenticate and authorize app rather than user. They pass along their Client ID and Client Secret to authenticate themselves and get a token.

6. What is Device Authorization Flow? The device asks user to go to link on their computer or smartphone and authorize device, in which they pass along their Client ID to initiate the authorization process and get a token.

7. What is Resource Owner Password Flow? Highly-trusted applications which requests that users provide credentials (username and password), typically using an interactive form.

_<a href = "https://auth0.com/docs/libraries/auth0-react">"Auth0 for single page apps"</a>_

The Auth0 React SDK (auth0-react.js) is a JavaScript library for implementing authentication and authorization in React apps with Auth0. It provides a custom React hook and other Higher Order Components so you can secure React apps using best practices while writing less code.

The Auth0 React SDK handles grant and protocol details, token expiration and renewal, as well as token storage and caching. Under the hood, it implements Universal Login and the Authorization Code Grant Flow with PKCE.

The library is hosted on GitHub where you can read more about the API.

**<a href = "https://github.com/scottie-l/reading-notes/tree/main/reading-notes-301">Back</a>**
