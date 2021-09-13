# Server Development Guidelines


## Web Services

### Interface

* All web request bodies should be JSON
* JSON web service requests without the ```application/json``` content type are invalid
* A web service response should always have the content type of ```application/json```
* A web service should never return HTML
* A web service response body should always be valid JSON, even if it is just an empty dictionary
* A web service should never return a redirect (any HTTP status code within the ```300``` range)
* Unless a web service is only consumed by an internal server infrastructure, web services should support versioning and have a required version parameter
* Never pass sensitive data such as user credentials in a URL.  Pass sensitive data through the HTTP body.
* Do not pass credentials on every request.  Use sessions/tokens
* The interface of an HTTP `get` request should be treated as immutable.  In other words, the functionality of an HTTP `get` request should never modify public server state.
  
    * Under the hood the server can change private server state when handling a `get` request such as caching `get` responses.
* URL paths should always place nouns before verbs

    * Bad: `run/app`

    * Good: `app/run`
* A web app should not use CORS to communicate with its own servers
* All web services should support CORS

## Database

* When querying data from a SQL database, perform all filtering in SQL, not server code.  Performing the filtering in SQL is:

    * More performant
    
    * More useful for database admins
        * A database admin can run snippets of SQL on a database, but cannot do so with JavaScript
    

## Testing

* Whenever practical, hard-code fixture ids. It makes testing easier and more predictable.