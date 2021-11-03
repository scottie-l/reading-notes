<b><a href = "https://docs.microsoft.com/en-us/azure/architecture/best-practices/api-design">"RESTful web API design"</a>

1. What does REST stand for? Representation State Transfer

2. REST APIs are designed around a what? Resources, a kind of object, data, or service that can be accessed by the client.

3. What is an identifer of a resource? A unique URI for that resource.
    - Give an example. https://adventure-works.com/orders/1

4. What are the most common HTTP verbs? GET, POST, PUT, PATCH, DELETE.

5. What should the URIs be based on? Should be based on Nouns (resource) and not the verbs.

6. Give an example of a good URI. /collection/item/collection.

7. What does it mean to have a ‘chatty’ web API? The client app sends multiple requests to find data it requires.
    - Is this a good or a bad thing? Making many requests can use up resources, but making too karge a request can use up bandwidth.

8. What status code does a successful GET request return? 200 (ok).

9. What status code does an unsuccessful GET request return? 404 (Not Found).

10. What status code does a successful POST request return? 201 (Created).

11. What status code does a successful DELETE request return? 204 (No Content).

The Open API Initiative was created by an industry consortium to standardize REST API descriptions across vendors. As part of this initiative, the Swagger 2.0 specification was renamed the OpenAPI Specification (OAS) and brought under the Open API Initiative.

To adopt OpenAPI for your web APIs, here are some points to consider:

- The OpenAPI Specification comes with a set of opinionated guidelines on how a REST API should be designed. That has advantages for interoperability, but requires more care when designing your API to conform to the specification.

- OpenAPI promotes a contract-first approach, rather than an implementation-first approach. Contract-first means you design the API contract (the interface) first and then write code that implements the contract.

- Tools like Swagger can generate client libraries or documentation from API contracts. For example, see ASP.NET Web API help pages using Swagger.

More information:
    - <a href = "https://github.com/Microsoft/api-guidelines/blob/master/Guidelines.md">Microsoft REST API guidelines.</a> Detailed recommendations for designing public REST APIs.
    - <a href = "https://mathieu.fenniak.net/the-api-checklist">Web API checklist.</a> A useful list of items to consider when designing and implementing a web API.
    - <a href = "https://www.openapis.org/">Open API Initiative.</a> Documentation and implementation details on Open API.

<b><a href = "https://regexr.com/">"Regexr"</a>

How would you match your name using RegEx? /scott leas.

RegExr was created by gskinner.com, and is proudly hosted by Media Temple.

PCRE & JavaScript flavors of RegEx are supported. Validate your expression with Tests mode.

The side bar includes a Cheatsheet, full Reference, and Help. You can also Save & Share with the Community, and view patterns you create or favorite in My Patterns.

Explore results with the Tools. Replace & List output custom results. Details lists capture groups. Explain describes your expression in plain English.

<b><a href = "https://medium.com/factory-mind/regex-tutorial-a-simple-cheatsheet-by-examples-649dc1c3f285">"Regexer Cheatsheet"</a>

Summary: As discussed, the application fields of regex can be multiple, here's a quick list:

- data validation (for example check if a time string i well-formed)
- data scraping (especially web scraping, find all pages that contain a certain set of words eventually in a specific order)
- data wrangling (transform data from “raw” to another format)
- string parsing (for example catch all URL GET parameters, capture text inside a set of parenthesis)
- string replacement (for example, even during a code session using a common IDE to translate a Java or C# class in the respective JSON object — replace “;” with “,” make it - - - lowercase, avoid type declaration, etc.)
- syntax highlightning, file renaming, packet sniffing and many other applications involving strings (where data need not be textual)

##### <b><a href = "https://regex101.com/">"Regexr 101"</a>

Link for site testing page!

<a href = "https://github.com/scottie-l/reading-notes/tree/main/reading-notes-301">Back</a>
