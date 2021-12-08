<b><a href = "https://www.sitepoint.com/an-introduction-to-node-js/">"Intro to Node.js"</a>

1. What is node.js? A JS runtime build that uses Googles V8 JS engine and library to execute JS on our computers.

2. In your own words, what is Chrome’s V8 JavaScript Engine? An open source JS engine that runs in Google and other Chromium based browsers.

3. What does it mean that node is a JavaScript runtime? Node.js is a program that we can use to execute JS on our computers.

4. What is npm? Node package manager.

5. What version of node are you running on your machine? v14.17.3

6. What version of npm are you running on your machine? v6.14.13

7. What command would you type to install a library/package called ‘jshint’? npm install -g jshint (global install, or for local install) npm init -y, in file, then npm install lodash --save.

8. What is node used for? installing and running various build tools — designed to automate the process of developing modern JavaScript application. Second common use is node.js lets us run JavaScript on the server. It can also be used as scripting language to automate repetitive or error prone tasks on your PC. As well as to write your own command line tool, such as this Yeoman-Style generator to scaffold out new projects. Node.js can also can be used to build cross-platform desktop apps and even to create your own robots.

What Is Node.js? This is what the project’s home page has to say: Node.js® is a JavaScript runtime built on Chrome’s V8 JavaScript engine.

And this is what Stack Overflow has to offer: Node.js is an event-based, non-blocking, asynchronous I/O runtime that uses Google’s V8 JavaScript engine and libuv library.

Node Is Built on Google Chrome’s V8 JavaScript Engine. The V8 engine is open-source JavaScript engine that runs in Google Chrome and other Chromium-based web browsers. Designed with performance in mind and is responsible for compiling JavaScript directly to native machine code that computer can execute. However, when we say that Node is built on V8 engine, we don’t mean that Node programs are executed in browser; They aren’t. Rather, Node took the V8 engine and enhanced it with various features, such as a file system API, an HTTP library, and a number of operating system–related utility methods.

This means that Node.js is a program we can use to execute JavaScript on our computers. In other words, it’s a JavaScript runtime.

Node Binaries vs Version Manager: Many websites will recommend that you head to the official Node download page and grab Node binaries for system. Would suggest that use a version manager instead. This is program that allows you to install multiple versions of Node and switch between them. There are advantages to using version manager. For example, negates potential permission issues when using Node with npm, and lets you set Node version on per-project basis.

How Do I Install Node.js? The Node.js Way: Check that Node is installed on system by opening a terminal and typing node -v. Should see something like v12.14.1 displayed. Next, create new file, hello.js and copy in following code:

console.log("Hello, World!"); This uses Node’s built-in console module to display message in terminal window. To run example, enter following command: node hello.js . If Node.js is configured properly, “Hello, World!” will be displayed.

Node.js Has Excellent Support for Modern JavaScript: Node has excellent support for ECMAScript 2015 (ES6) and beyond. As only targeting one runtime (specific version of V8 engine), this means you can write JavaScript using latest and most modern syntax. Also means you don’t generally have to worry about compatibility issues.

Introducing npm, the JavaScript Package Manager: Node comes bundled with package manager called npm. To check which version you have installed on system, type npm -v. In addition to being package manager for JavaScript, npm is also world’s largest software registry. There are over 1,000,000 packages of JavaScript code available to download, with billions of downloads per week. How to use npm to install package.

Installing a Package Globally: Open terminal and type the following: npm install -g jshint

This will install jshint package globally on system. Can use it to lint the index.js file.

jshint index.js ;Should see number of ES6-related errors. To fix, add /* jshint esversion: 6 */ to the top of the index.js file, re-run the command and linting should pass.

Installing a Package Locally: Can also install packages locally to project on our system. Create test folder and open terminal in that directory. Next type: npm init -y . This will create and auto-populate package.json file in same folder. Next, use npm to install lodash package and save as project dependency:

npm install lodash --save

Create file named test.js and add following: const _ = require('lodash');

const arr = [0, 1, false, 2, '', 3];

console.log(_.compact(arr));

Finally, run script using node test.js. Should see [ 1, 2, 3 ] output to terminal.

Working with the package.json File: Folder entitled node_modules. This is where npm has saved lodash and any libraries that lodash depends on. The node_modules folder shouldn’t be checked in to version control, and in fact, be re-created at any time by running, npm install, from within the project’s root.

If open package.json file, See lodash listed under dependencies field. By specifying project’s dependencies in this way, you'll allow any developer anywhere to clone project and use npm to install whatever packages it needs to run.

What Is Node.js Used For? The first of their common uses: installing (via npm) and running (via Node) various build tools — designed to automate the process of developing a modern JavaScript application. Second common use is node.js lets us run JavaScript on the server.

These build tools come in all shapes and sizes, and you won’t get far in modern JavaScript landscape without bumping into them. They can be used for anything from bundling your JavaScript files and dependencies into static assets, to running tests, or automatic code linting and style checking.

Node.js Lets Us Run JavaScript on the Server: Next we come to one of the biggest use cases for Node.js — running JavaScript on the server. Node.js, provides some unique benefits, compared to traditional languages. Node plays critical role in technology stack of many high-profile companies.

Benefits are: The Node.js Execution Model - In very simplistic terms, when you connect to a traditional server, such as Apache, it will spawn a new thread to handle the request. In a language such as PHP or Ruby, any subsequent I/O operations block the execution of your code until the operation has completed. That is, the server has to wait for the database lookup to complete before it can move on to processing the result. If new requests come in while this is happening, the server will spawn new threads to deal with them. This is potentially inefficient, as a large number of threads can cause a system to become sluggish — and, in the worst case, for the site to go down. The most common way to support more connections is to add more servers.

Node.js, however, is single-threaded. It’s also event-driven, which means that everything that happens in Node is in reaction to an event. For example, when a new request comes in the server will start processing it. If it then encounters a blocking I/O operation, instead of waiting for this to complete, it will register a callback before continuing to process the next event. When the I/O operation has finished, the server will execute the callback and continue working on the original request. Under the hood, Node uses the libuv library to implement this asynchronous (that is, non-blocking) behavior.

Node’s execution model causes the server very little overhead, and consequently it’s capable of handling a large number of simultaneous connections. The traditional approach to scaling a Node app is to clone it and have the cloned instances share the workload. Node.js even has a built-in module to help you implement a cloning strategy on a single server.

Are There Any Downsides? The fact that Node runs in a single thread does impose some limitations. For example, blocking I/O calls should be avoided, CPU-intensive operations should be handed off to a worker thread, and errors should always be handled correctly for fear of crashing the entire process. Some developers also dislike the callback-based style of coding that JavaScript imposes. But with the arrival of native Promises, followed closely by async await, flow control in modern JavaScript has become easier than it ever was.

What Kind of Apps Is Node.js Suited To? Node is particularly suited to building applications that require some form of real-time interaction or collaboration — for example, chat sites, or apps such as CodeShare, where you can watch a document being edited live by someone else. It’s also a good fit for building APIs where you’re handling lots of requests that are I/O driven, or for sites involving data streaming, as Node makes it possible to process files while they’re still being uploaded.

Yet saying this, not everyone is going to be building the next Trello or the next Google Docs, and really, there’s no reason that you can’t use Node to build a simple CRUD app. However, if you follow this route, you’ll soon find out that Node is pretty bare-bones and that the way you build and structure the app is left very much up to you. There are various frameworks you can use to reduce the boilerplate, with Express having established itself as the front runner. Yet even a solution such as Express is minimal, meaning that if you want to do anything slightly out of the ordinary, you’ll need to pull in additional modules from npm. This is in stark contrast to frameworks such as Rails or Laravel, which come with a lot of functionality out of the box.

What Are the Advantages of Node.js? Aside from speed and scalability, an often-touted advantage of using JavaScript on a web server — as well as in the browser — is that your brain no longer needs to switch modes. You can do everything in the same language, which, as a developer, makes you more productive.

Another of Node’s big pluses is that it speaks JSON. JSON is probably the most important data exchange format on the Web, and the lingua franca for interacting with object databases. JSON is ideally suited for consumption by a JavaScript program, meaning that when you’re working with Node, data can flow neatly between layers without the need for reformatting. You can have one syntax from browser to server to database.

Finally, JavaScript is ubiquitous: most of us are familiar with JavaScript, or have used it at some point. This means that transitioning to Node development is potentially easier than to other server-side languages.

Other Uses of Node: It can be used as a scripting language to automate repetitive or error prone tasks on your PC. It can also be used to write your own command line tool, such as this Yeoman-Style generator to scaffold out new projects. Node.js can also can be used to build cross-platform desktop apps and even to create your own robots.

Conclusion: Node.js is an event-based, non-blocking, asynchronous I/O runtime that uses Google’s V8 JavaScript engine and libuv library.

<b><a href = "https://www.codefellows.org/blog/6-reasons-for-pair-programming/">"6 reasons for pair programming"</a>

1. What are the 6 reasons for pair programming? Greater efficiency, Engaged collaboration, Learning from fellow developers, Social skills, job interview readiness, & work environment readiness.

2. In your experience, which of these reasons have you found most beneficial? The ability to learn my fellow students/devs.

3. How does pair programming work? One person is Driver who types the code in terminal, or text editor, while the other person is Navigator who guides the driver and researches while driver is typing.

Pair programming is the practice of two developers sharing a single workstation to interactively tackle a coding task together.

How does pair programming work? While there are many different styles, pair programming commonly involves two roles: the Driver and the Navigator. The Driver is the programmer who is typing and the only one whose hands are on the keyboard. The Driver manages the text editor, switching files, version control, and—of course writing—code. The Navigator uses their words to guide Driver but does not provide any direct input to computer. The Navigator thinks about the big picture, what comes next, how an algorithm might be converted in to code, while scanning for typos or bugs. The Navigator might also utilize their computer as a second screen to look up solutions and documentation, but should not be writing any code.

Why pair program? While learning to code, developers likely study several programming languages. Similar to a foreign language class, there are four fundamental skills that help anyone learn a new language:

- Listening: hearing and interpreting the vocabulary
- Speaking: using the correct words to communicate an idea
- Reading: understanding what written language intends to convey
- Writing: producing from scratch a meaningful, well structured script

Pair programming touches on all four skills: developers explain out loud what the code should do, listen to others’ guidance, read code that others have written, and write code themselves. During a five-hour paired lab session, Code Fellows students work on all four of these language-specific skills.

1. Greater efficiency - It is a common misconception that pair programming takes a lot longer and is less efficient. In reality, when two people focus on the same code base, it is easier to catch mistakes in the making. Research indicates that pair programing takes slightly longer, but produces higher-quality code that doesn’t require later effort in troubleshooting and debugging. So, in the long-run, it’s often actually more efficient than two people working on separate features. When coming up with ideas and discussing solutions out loud, two programmers may come to a solution faster than one programmer on their own. Also, when the pair is stuck, both programmers can research the problem and reach a solution faster. Researches also identified pairing enhances technical skills, team communication, and even enjoyability of coding in the workplace.

2. Engaged collaboration - When two programmers focus on the same code, the experience is more engaging and both programmers are more focused than if they were working alone. It is harder to procrastinate or get off track when someone else is relying on you to complete the work. Popping open your Facebook timeline is just that less enticing when someone else is looking at your screen. Another important aspect of learning to program is knowing when to ask for help. We advise our students to spend no more than fifteen minutes stuck on a problem before asking a teaching assistant or instructor for help. When developers pair program, they rely more on each other and can often find a solution together without needing to ask for additional help.

3. Learning from fellow students - Everyone has a different approach to problem solving; working with a teammate can expose developers to techniques they otherwise would not have thought of. If one developer has a unique approach to a specific problem, pair programming exposes the other developer to a new solution. Often times, the developers in a pairing have different skill sets. If one programmer is more experienced in a certain skill, they can teach a student who is less familiar with that area. The less experienced developer benefits from the experienced developer’s knowledge and guidance, and the latter benefits from explaining the topic in their own words, further solidifying their own understanding.

4. Social skills - Pair programming is great for improving social skills. When working with someone who has a different coding style, communication is key. This can become more difficult when two programmers have different personalities. Pair programming not only improves programming skills, but can also help programmers develop their interpersonal skills. When just grabbing the keyboard and taking over isn’t an option, getting good at finding the right words is a skill unto itself. This has long-term career impacts. As much as employers want strong programmers, they know it’s essential to hire people who can work well with others.

5. Job interview readiness - A common step in many interview processes involves pair programming between a current employee and an applicant, either in person or through a shared screen. They will carry out exercises together, such as code challenges, building a project or feature, or debugging an existing code base. By doing so, companies can get a better feel for how an applicant will fit into the team and their collaboration style. For most roles, the ability to work with and learn from others and stellar communication skills are as important to a company than specific technical skills. Pair programming strengthens all of those skills.

6. Work environment readiness - Many companies that utilize pair programing expect to train fresh hires from CS-degree programs on how they operate to actually deliver a product. Code Fellows graduates who are already familiar with how pairing works can hit the ground running at a new job, with one less hurdle to overcome.

<b><a href = "https://locationiq.com/">"Geocoding API Docs"</a>

<b><a href = "https://www.npmjs.com/package/axios">"Axios Docs"</a>

<b><a href = "https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Asynchronous/Async_await">"MCN async and await"</a>

<a href = "https://github.com/scottie-l/reading-notes/tree/main/reading-notes-301">Back</a>
