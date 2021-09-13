# Code Style

* In general, use camelCase.

    * Table names should be snake_case.
    
    * File names should be kebab-case.
    
    * Environment variable names should be ALL_CAPS_SNAKE_CASE
* Never directly refer to a hard-coded id value within a function body.  Assign those values to global constants or enums and refer to those within your functions.
* Only use abbreviations when they are so common they are industry standards across many programming languages such as `db` and `config`.
* When iterating over the keys of an object, iterate over the  `Object.keys` of that object
    * Example: `for (const key of Object.keys(foo))`
