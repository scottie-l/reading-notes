# Notes - Day 30

1. What are the advantages of storing tokens in “Cookies” vs “Local Storage”? Easier to implement cookies, and can be used to make API calls, or visit other sites using same session cookie, which won't work if using local storage. Malicious code can be injected to get the data from local storage, but setting the `httpOnly` flag stops the code from being available on the front end. <a href = "https://supertokens.com/blog/cookies-vs-localstorage-for-sessions-everything-you-need-to-know">"Source"</a>

2. Explain 3rd party cookies? Third-party cookies are cookies that are set by a website other than the one you are currently on. For example, you can have a "Like" button on your website which will store a cookie on a visitor's computer, that cookie can later be accessed by Facebook to identify visitors and see which websites they visited. <a href = "https://cookie-script.com/all-you-need-to-know-about-third-party-cookies.html#:~:text=Third%2Dparty%20cookies%20are%20cookies,see%20which%20websites%20they%20visited.">"Source"</a>

3. How do pixel tags work? Pixel tags, or, web beacons, as they are also known, attach to a browser and collect information about an anonymous user's movements on the Internet. They allow sites to provide users with ads for services and products that are relevant to them.  <a href = "https://abcnews.go.com/Technology/We_Find_Them/pixel-tags-threaten-online-privacy-security/story?id=14809833">"Source"</a>

4. Document the following Vocabulary Terms:

- <u>*cookies:*</u> Cookies are data, stored in small text files, on your computer. When a web server has sent a web page to a browser, the connection is shut down, and the server forgets everything about the user. <a href = "https://www.w3schools.com/js/js_cookies.asp#:~:text=Cookies%20are%20data%2C%20stored%20in,forgets%20everything%20about%20the%20user.">"Source"</a>
- <u>*authorization:*</u> The HTTP Authorization request header can be used to provide credentials that authenticate a user agent with a server, allowing access to a protected resource. The Authorization header is usually, but not always, sent after the user agent first attempts to request a protected resource without credentials. <a href = "https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Authorization">"Source"</a>
- <u>*access control:*</u> Role-based access control, also known as role-based security, is a mechanism that restricts system access to users using their roles and privileges and permissions. Within an application, roles are created for various user types <a href = "https://blog.logrocket.com/using-accesscontrol-for-rbac-and-abac-in-node-js/#:~:text=Role%2Dbased%20access%20control%2C%20also,e.g.%2C%20writer%20or%20reader).">"Source"</a>
- <u>*conditional rendering:*</u> Conditional rendering is a term to describe the ability to render different user interface (UI) markup if a condition is true or false. In React, it allows us to render different elements or components based on a condition. This concept is applied often in the following scenarios: Rendering external data from an API. <a href = "https://www.digitalocean.com/community/tutorials/7-ways-to-implement-conditional-rendering-in-react-applications">"Source"</a>

---
<a href = "https://github.com/scottie-l/reading-notes/tree/main/reading-notes-401">Back</a>

---
