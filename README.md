### Install

```
npm install js.cookie --save
```

### Usage

```javascript

import Cookie from "js.cookie";

// Set cookie

Cookie.set(
	"name",                                       // @string
	"john",                                       // @string, @number, @object
	{                                             // @object (options, not necessary)
		domain:  "example.com",                   // @string                 | default: current domain
		path:    "/path",                         // @string                 | default: "/"
		secure:  true,                            // @boolean                | default: false
		expires: "Tue, 19 Jan 2038 03:14:07 GMT", // @string (in GMT format) | default: session cookie
		live:    1                                // @number (days of life)  | default: session cookie
	}
);                                                // > "john" | @string


// Get cookie

Cookie.get( "name" );                             // > "john" | @string

// Remove cookie

Cookie.remove( "name" );                          // > "john" | @string
Cookie.get( "name" );                             // > undefined

```

### More

```javascript

Cookie.set( "obj", {foo: "bar"} );                // > {foo: "bar"} | @object

Cookie.get( "obj" );                              // > {foo: "bar"} | @object

Cookie.set( "num", 1 );                           // > 1            | @number

Cookie.get( "num" );                              // > 1            | @number

```