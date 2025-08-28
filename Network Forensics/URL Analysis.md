URL Analysis - Activity that is performed to identify whether a link is already flagged on an existing reputation list and, if not, to identify what malicious script or activity might be coded within in.

HTTP Method - A set of request methods to indicate the desired action to be performed for a given resource.
- GET - Principal method used to retrieve a resource
- POST - Used to send data to the server for processing
- PUT - Creates or replaces the requested resource
- DELETE - Used to remove the requested resource
- HEAD - Retrieves the headers for a resource only and ignores the body
Data submitted via a URL is delimited by the '?' character
Query parameters are usually formatted as one or more name=value pairs with '&' delimiting each pair.
A '#' is used to indicate a fragment or anchor ID and it's not processed by the web server.

HTTP Response Codes - The header value returned by a server when a client requests a URL
- 200 - Indicates a successful GET or POST request
- 201 - Indicates a PUT request has been successful in creating a resource
- 3xx - Any code in this range indicates a redirect has occurred
- 4xx - Any code in this range indicates an error in the client request
	- 400 - Request could not be parsed by server
	- 401 - Indicates that a request did not supply the authentication credentials
	- 403 - Indicates that a request did not have sufficient permissions
	- 404 - Indicates that a client has request a non-existent resource
- 5xx - Any code in this range indicates a server-side issue
	- 500 - Indicates a general error on the server-side of the application
	- 502 - Indicates a bad gateway has occurred when the server is acting as a proxy
	- 503 - Indicates an overloading of the server causing service unavailability
	- 504 - Indicates a gateway timeout which means there's an issue with the upstream server

Percent (URL) Encoding - Mechanism to encode 8-bit characters that have specific meaning in the context of URLs.
A URL can contain only unreserved and reserved characters from the ASCII set.
Unreserved Characters:
- a-z
- A-Z
- 0-9
- -
- .
- _
- ~
Reserved Characters:
- :
- /
- ?
- `#`
- `[]`
- @
- !
- $
- &
- '
- ()
- `*`
- +
- ,
- ;
- =

A URL cannot contain unsafe characters. Null string termination, carriage return, line feed, end of file, tab, space, and `/ <> {}`

Percent (URL) encoding allows a user agent to submit any safe or unsafe character (or binary data) to the server within a URL.

**Warning** - Percent encoding can be misused to obfuscate the nature of a URL, like encoding unreversed characters and submitting malicious input as a script or binary to perform directory traversal

Character | Percent Encoding pairs:
- null | %00
- space | %20
- + | %2B
- % | %25
- / | %2F
- \ | %5C
- . | %2E
- ? | %3F
- " | %22
- ' | %27
- < | %3C
- > | %3E

