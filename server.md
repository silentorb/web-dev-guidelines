# Server Development Guidelines


## Web Services

### Interface

* All web request bodies should be JSON
* JSON web service requests without the ```application/json``` content type are invalid
* A web service response should always have the content type of ```application/json```
* A web service should never return HTML
* A web service response body should always be valid JSON, even if it is just an empty dictionary
* A web service should never return a redirect (any HTTP status code within the ```3XX``` range)
* Unless a web service is only consumed by an internal server infrastructure, web services should support versioning and have a required version parameter
* Sensitive data such as user credentials should not be passed in a URL
    * Instead, sensitive data should be passed using an HTTP body
* Do not pass credentials on every request.  Use sessions/tokens
* The interface of an HTTP `get` request should be treated as immutable.  In other words, the functionality of an HTTP `get` request should never modify public server state.
  
    * Under the hood the server can change private server state when handling a `get` request such as caching `get` responses.
* URL paths should always place nouns before verbs

    * Bad: `run/app`

    * Good: `app/run`
* A web app should not use CORS to communicate with its own servers
* All web services should support CORS
* Static content should not be served through Node.js, unless it is reverse-proxying a service that requires specialized business logic such as advanced authorization
    * Instead, use a service like S3+Cloudfront

## Database

* When querying data from a SQL database, most filtering should be perfomed in SQL, not server code.  Performing the filtering in SQL is:

    * More performant
    
    * More useful for database admins
        * A database admin can run snippets of SQL on a database, but cannot do so with JavaScript
    

## Testing

* Whenever practical, hard-code fixture ids
  * Doing so makes testing easier and more predictable
