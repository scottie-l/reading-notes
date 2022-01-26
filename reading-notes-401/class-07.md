# Notes - Day 7

1. Write the following steps in the correct order:

- Register your application to get a client_id and client_secret
- Ask the client if they want to sign in via a third party
- Make a request to a third-party API endpoint
- Receive access token
- Receive authorization code
- Make a request to the access token endpoint
- Redirect to a third party authentication endpoint

2. What can you do with an authorization code? With authorization code you can make a request to get an access token.

3. What can you do with an access token? Allow access to sensitive/secure data or areas.

4. What’s a benefit of using OAuth instead of your own basic authentication? It decouples authentication from authorization and supports multiple use cases addressing different device capabilities. It supports server-to-server apps, browser-based apps, mobile/native apps, and consoles/TVs. <a href = "https://developer.okta.com/blog/2017/06/21/what-the-heck-is-oauth#:~:text=It%20enables%20apps%20to%20obtain,apps%2C%20and%20consoles%2FTVs.">"Source"</a>

5. Document the following Vocabulary Terms:

- *Client ID:* A Client ID is an identifier associated with an application that assists with client / server OAuth 2.0 authentication for ArcGIS client APIs. <a href = "https://developers.arcgis.com/documentation/glossary/client-id/">"Source"</a>
- *Client Secret:* Client Secret (OAuth 2.0 client_secret) is a secret used by the OAuth Client to Authenticate to the Authorization Server. The Client Secret is a secret known only to the OAuth Client and the Authorization Server. Client Secret must be sufficiently random to not be guessable. <a href = "https://ldapwiki.com/wiki/Client%20Secret#:~:text=Client%20Secret%20(OAuth%202.0%20client_secret,random%20to%20not%20be%20guessable.">"Source"</a>
- *Authentication Endpoint:* Endpoint authentication is a security mechanism designed to ensure that only authorized devices can connect to a given network, site or service. <a href = "https://whatis.techtarget.com/definition/endpoint-authentication#:~:text=Endpoint%20authentication%20is%20a%20security,also%20known%20as%20device%20authentication.&text=Authenticating%20both%20the%20user%20and,%2Dfactor%20authentication%20(2FA).">"Source"</a>
- *Access Token Endpoint:* The token endpoint is where apps make a request to get an access token for a user. This section describes how to verify token requests and how to return the appropriate response and errors. <a href = "https://www.oauth.com/oauth2-servers/access-tokens/#:~:text=Access%20tokens%20are%20the%20thing,on%20behalf%20of%20a%20user.&text=The%20token%20endpoint%20is%20where,the%20appropriate%20response%20and%20errors.">"Source"</a>
- *API Endpoint:* An API Endpoint is a specific “point of entry” in an API and is the most crucial part of an API’s documentation. Endpoints are the main thing you’ll be using to make requests. So if an API’s endpoints aren’t listed clearly in the documentation, the API is essentially unusable. <a href = "https://apipheny.io/api-endpoint/">"Source"</a>
- *Authorization Code:*  An authorization code is typically a sequence of letters, numbers, or a combination of both, that validates a person's identity, approves a transaction or provides access to a secured area. <a href = "https://www.investopedia.com/terms/a/authorization-code.asp">"Source"</a>
- *Access Token:* In computer systems, an access token contains the security credentials for a login session and identifies the user, the user's groups, the user's privileges, and, in some cases, a particular application. <a href = "https://en.wikipedia.org/wiki/Access_token">"Source"</a>

<a href = "https://github.com/scottie-l/reading-notes/tree/main/reading-notes-401">**Back**</a>
