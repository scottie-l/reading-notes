<b><a href = "https://www.moesif.com/blog/technical/api-design/Which-HTTP-Status-Code-To-Use-For-Every-CRUD-App/">"Status Codes Based On REST Methods"</a>

1. In your own words, describe what each group of status code represents:

2. 100’s = Informational status codes, usually saying the head portion was received.

3. 200’s = Success codes. Signifies the request was accepted.

4. 300’s = Redirect codes. The resource is not in current location.

5. 400’s = Client error codes. Invalid requests from client sent to server.

6. 500’s = Server erroe codes. Indicate a problem with the server side.

7. What is a status code 202? Accepted. Often used with async function.

8. What is a status code 308? Pemanent Redirect. Tells them a new URL to go to.

9. What code would you use if an update didn’t return data to a client? 204.

10. What code would you use if a resource used to exist but no longer does? 308.

11. What is the ‘Forbidden’ status code? 403.

CRUD (Create, Read, Update, Delete)

The CRUD model defines the most basic API actions for persistent storage. Create, read, update, and delete. They make up the lions-share of API endpoints. Let’s see which - status codes meet their requirements.

- Create: 200, 201, 202, 303
- Read: 200, 206, 300, 308, 304, 307
- Update: 200, 204, 202
- Delete: 200, 204,202

Conclusion:

The HTTP creators thought about many status codes when designing it and even added a bunch of new ones over the years. If they’re used correctly they can help to improve developer experience greatly by leveraging automatic redirect follows of clients and explaining what happened more clearly.

Sometimes there are multiple codes we could use for one particular case, the important thing is that we keep our usage consistent over the whole API surface.

<b><a href = "https://www.youtube.com/channel/UCFbNIlppjAuEX4znoulh0Cw">"Build A REST API With Node.js, Express, & MongoDB - Video - 1st 20 minutes"</a>

1. Why do we need to pull our MongoDB database string out of our server and put it into our .env? It's a localhost variable, so will only connect to local computer, not remote.

2. What is middleware? Code that gets run when server gets request, but before it goes to routes.

3. What does app.use(express.json()) do? Allows us to use middleware.

4. What does the /:id mean in a route? It means that it's a parameter.

5. What is the difference beween PUT and PATCH? Put creates new entry in router. Patch will update just 1 field, not entire entry.

6. How do you make a defalut value in a schema? default: Date.now(or other value you want defaulted).

7. What does a 500 error status code mean? There is an error on the server, not the user or client.

8. What is the difference between a status 200 and a status 201? 201 means successfully created object, whereas 200 just means a successful connection.

<a href = "https://github.com/scottie-l/reading-notes/tree/main/reading-notes-301">Back</a>
