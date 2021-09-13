# TypeScript

* Avoid classes when possible
  * Use plain data interfaces instead
  * Sometimes classes are needed when used by a third party library
  * TypeScript annotations require classes
* Directories with code should have an `index.ts` file
  * Imports should use the shorter index path
    * Sometimes IDE auto import insertion gets confused and does not use the shorter path.  It is sometimes more practical occasionally perform general import cleanup instead of trying to ensure every pull request has perfect imports.
* Avoid files importing files in the same directory via absolute paths
  * This can cause circular dependency problems which result in incomplete imports at runtime
* Within a file, dependent functions should appear after the functions they depend on.
* Use `undefined` instead of `null` when possible
  * This is a complicated issue with a lot of caveats (https://basarat.gitbooks.io/typescript/docs/javascript/null-undefined.html)
* Avoid default exports (https://basarat.gitbooks.io/typescript/content/docs/tips/defaultIsBad.html)