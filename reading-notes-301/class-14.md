<b><a href = "https://www.csoonline.com/article/3216404/what-is-oauth-how-the-open-authorization-framework-works.html">"What is OAuth"</a>

1. What is OAuth? An open-standard authorization protocol or framework that describes how unrelated servers and services can safely authenticate access to their assets without actually sharing initial, related, single logon credential.

2. Give an example of what using OAuth would look like. When you go to log onto a website and it offers to log on using another website’s/service’s logon. You then click on the button linked to the other website, the other website authenticates you, and the website you were originally connecting to logs you on itself afterward using permissions gained from the second website.

3. How does OAuth work? OAuth essentially allows the user, via an authentication provider that they have previously successfully authenticated with, to give another website/service a limited access authentication token for authorization to additional resources.

- What are the steps that it takes to authenticate the user? Website A connects to the website B on behalf of the user, using OAuth, providing the user’s verified identity. Website B generates a one-time token and a one-time secret unique to the transaction and parties involved. Website A gives this token and secret to the initiating user’s client software. Client’s software presents the request token and secret to their authorization provider. If not already authenticated to the authorization provider, the client may be asked to authenticate. After authentication, the client is asked to approve the authorization transaction to the website B. The user approves (or software silently approves) a particular transaction type at website A. User is given an approved access token. The user gives the approved access token to website A. Website A gives the access token to website B as proof of authentication on behalf of user. Website B lets website A access their site on behalf of the user.

4. What is OpenID? 



<b><a href = "https://auth0.com/docs/authorization/flows">"Authorization and Authentication flows"</a>

1. What is the difference between authorization and authentication?

2. What is Authorization Code Flow?

3. What is Authorization Code Flow with Proof Key for Code Exchange (PKCE)?

4. What is Implicit Flow with Form Post?

5. What is Client Credentials Flow?

6. What is Device Authorization Flow?

7. What is Resource Owner Password Flow?



<b><a href = "https://auth0.com/docs/libraries/auth0-react">"Auth0 for single page apps"</a>



<a href = "https://github.com/scottie-l/reading-notes/tree/main/reading-notes-301">Back</a>
