# Code Style

* In general, use camelCase

    * Use PascalCase for type names
    * Table names should appear as lower snake_case in SQL
    * Table names in TypeScript/JavaScript should be PascalCase
    * File names should be lower kebab-case
    * Environment variable names should be ALL_CAPS_SNAKE_CASE
    
* Avoid starting lines of source code with parenthesis

* Avoid semi-colons when possible

    * Semi-colons are an outdated artifact of certain parser technical limits in the 70s

    * For depicing statement endings, semicolons are not as distinct as a newline (and indentation for multiline statements)

    * Scripting languages like Python and Functional languages like Haskell have demonstrated that semicolons are not needed and simply additional noise

    * Most programming languages created since 2010 either don't use semicolons or don't require them

    * Some of the common arguments in favor of JavaScript semicolons use bad code examples such as starting a line of code with parenthesis

        * ```javascript
            const a = foo
            (c + b).toString()
            ```

        * Code like that should be avoided

* Never directly refer to a hard-coded id value within a function body.  Assign those values to global constants or enums and refer to those within your functions.

* Only use abbreviations when they are so common they are industry standards across many programming languages such as `db` and `config`.

* When iterating over the keys of an object, iterate over the  `Object.keys` of that object
    
    * Example: `for (const key of Object.keys(foo))`
