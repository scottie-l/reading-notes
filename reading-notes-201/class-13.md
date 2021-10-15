<a href = "http://diveinto.html5doctor.com/storage.html">"The Past, Present & Future of Local Storage for Web Applications"</a>

Persistent local storage is an area where native client apps have an advantage over web apps. Native apps, the OS typically provides an abstraction layer for storing and retrieving app-specific data like preferences or runtime state. The values may be stored in the registry, INI files, XML files, or some other place according to platform convention. If native client app needs local storage beyond key/value pairs, can embed your database, invent own file format, or any number of other solutions.

Web apps don't have that. Cookies invented early in the web’s history, and can be used for persistent local storage of small amounts of data. Have three downsides: 1) Cookies included with every HTTP request, slowing down web app by needlessly transmitting same data over and over. 2) Cookies included with every HTTP request, sending data unencrypted over the internet (unless your entire web application is served over SSL). 3) Cookies limited to about 4KB of data — enough to slow down your application, but not enough to be terribly useful

What we want: a lot of storage space. On the client. Persists beyond page refresh. And isn't transmitted to server. All this prior to HTML5.

Microsoft invented things for browser that included DHTML behaviors & user Data.

userData: allows webpage to store up to 64KB of data/domain, in hierarchal XML-based structure. No permissions dialog, and no allowance for increase.

In '02 adobe introduced feature in Flash 6 called 'Flash Cookies'. Properly called 'Local Shared Objects'. Allows Flash objects to store up to 100 KB of data per domain. In '06, the advent of ExternalInterface in Flash 8, accessing LSOs from JavaScript became an order of magnitude easier and faster. Flash gives each domain 100 KB of storage for 'free'. Beyond that, prompts user for each order of magnitude increase in data storage.

'07, Google launched 'Gears', open source browser plugin aimed at providing additional capabilities in browsers. Gears provides API to an embedded SQL database based on SQLite. After obtaining permission from user once, Gears can store unlimited amounts of data per domain in SQL database tables.

Brad Neuberg and others continued to hack dojox.storage to provide unified interface to all different plugins and APIs. By '09, dojox.storage could auto-detect Adobe Flash, Gears, Adobe AIR, and early prototype of HTML5 storage that was only implemented in older versions of Firefox.

As you survey solutions, pattern emerges: all of them are either specific to single browser, or reliant on third-party plugin. Despite efforts to paper over the differences, they all expose radically different interfaces, have different storage limitations, and present different user experiences. This is problem that HTML5 set out to solve provide a standardized API, implemented natively and consistently, in multiple browsers, without having to rely on third-party plugins.

“HTML5 Storage” is specification named Web Storage, which was at one time part of the HTML5 specification proper, but split into its specification for uninteresting political reasons. Browser vendors also refer to it as 'Local Storage or 'DOM Storage'. Naming situation made even more complicated by some related, similarly-named, emerging standards.

What is HTML5 Storage? It’s way for web pages to store named key/value pairs locally, within the client web browser. Like cookies, data persists even after you navigate away from web site, close your browser tab, exit your browser, etc. Unlike cookies, this data never transmitted to remote web server. Unlike previous attempts at providing persistent local storage, it's implemented natively in web browsers, so it's available even when third-party browser plugins are not.

From JavaScript code, access HTML5 Storage through localStorage object on global window object. Before you can use it, should detect whether browser supports it.

function supports_html5_storage() {

  try {

    return 'localStorage' in window && window['localStorage'] !== null;

  } catch (e) {

    return false;

  }

}

HTML5 Storage based on named key/value pairs. Store data based on named key, then can retrieve that data with same key. Named key is string. Data can be any type supported by JavaScript, including strings, Booleans, integers, or floats. However, data is actually stored as string. If you are storing and retrieving anything other than strings, you'll need to use functions like parseInt() or parseFloat() to coerce your retrieved data into expected JavaScript datatype.

interface Storage {

  getter any getItem(in DOMString key);

  setter creator void setItem(in DOMString key, in any data);

};

Calling setItem() with named key that already exists will overwrite previous value. Calling getItem() with non-existent key will return null rather than throw exception.

Like other JavaScript objects, can treat localStorage object as associative array. Instead of using the getItem() and setItem() methods, can use square brackets.

Also method for removing value for given named key, and clearing entire storage area.

interface Storage {

  deleter void removeItem(in DOMString key);

  void clear();

};

Calling removeItem() with a non-existent key will do nothing.

Property to get total number of values in storage area, and iterate through all keys by index to get the name of each key.

interface Storage {

  readonly attribute unsigned long length;

  getter DOMString key(in unsigned long index);

};

If you call key() with index that isn't between 0–(length-1), function will return null.

If want to keep track programmatically when storage area changes, can trap the storage event. Storage event is fired on window object whenever setItem(), removeItem(), or clear() called and actually changes something. Example, you set item to existing value or call clear() when there are no named keys, the storage event will not fire, because nothing actually changed in storage area.

Storage event is supported everywhere localStorage object is supported, which includes Internet Explorer 8. IE 8 does not support the W3C standard addEventListener. Therefore, to hook the storage event, need to check which event mechanism browser supports. 

if (window.addEventListener) {

  window.addEventListener("storage", handle_storage, false);

} else {

  window.attachEvent("onstorage", handle_storage);

};

handle_storage callback function will be called with StorageEvent object, except in Internet Explorer where the event object is stored in window.event.

function handle_storage(e) {

  if (!e) { e = window.event; }

}

At this point, variable e will be StorageEvent object, which has following useful properties.

'5 megabytes' is the limit to storage space each origin gets by default. Is surprisingly consistent across browsers. Keep in mind you’re storing strings, not data in its original format. If storing lots of integers or floats, difference in representation can add up. Each digit in float is being stored as character, not in usual representation of floating point number.

“QUOTA_EXCEEDED_ERR” is exception that will get thrown if you exceed your storage quota of 5 megabytes. “No” is the answer to the next obvious question, 'Can I ask the user for more storage space?' At time of writing (February 2011), no browser supports any mechanism for web developers to request more storage space. Some browsers allow user to control each site’s storage quota, but it is purely a user-initiated action, not something that you as a web developer can build into your web application.

A new API has standardized and implemented across all major browsers, platforms, and devices.

One vision is acronym that you probably know already: SQL. In '07, Google launched Gears, open source cross-browser plugin which included an embedded database based on SQLite. This early prototype later influenced the creation of Web SQL Database specification. Web SQL Database provides thin wrapper around SQL database, allowing you to do things like this from JavaScript: actual working code in 4 browsers

openDatabase('documents', '1.0', 'Local document storage', 5*1024*1024, function (db) {

  db.changeVersion('', '1.0', function (t) {

    t.executeSql('CREATE TABLE docids (id, name)');

  }, error);

});

There is actual SQL specification (called SQL-92), but there is no database server in world that conforms to that and only that specification. Each of these products adds new SQL features over time, so saying “SQLite’s SQL” is not sufficient to pin down exactly what you’re talking about. Need to say 'the version of SQL that shipped with SQLite version X.Y.Z.'.

Introduce another competing vision for advanced, persistent, local storage for web apps: Indexed Database API, formerly known as “WebSimpleDB,” now affectionately known as “IndexedDB.”

Indexed Database API exposes what’s called object store. Object store shares many concepts with SQL database. There are 'databases' with 'records', and each record has set number of 'fields'. Each field has specific datatype, which is defined when database is created. Can select subset of records, enumerate them with 'cursor'. Changes to object store handled within 'transactions'.

Primary difference is the object store has no structured query language. You don’t construct statement like 'SELECT * from USERS where ACTIVE = 'Y'. Instead, use methods provided by object store to open cursor on database named 'USERS', enumerate through records, filter out records for inactive users, and use accessor methods to get values of each field in remaining records.

At time of writing, IndexedDB has only been implemented in beta version of Firefox 4.

<a href="https://github.com/scottie-l/Reading-notes-201">Back</a>