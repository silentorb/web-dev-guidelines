# Git Workflow

## When Submitting a PR

* Commit messages should be meaningful and distinct
* Break large tasks into multiple PRs
* When working on multiple feature branches in parallel, ensure that none of the branches depend on each for at least partial functionality
  * This sometimes requires additional abstractions to loosely couple the individual features.
  * It is easier to work on features sequentially than in parallel
  * Parallel development requires additional overhead
* When practical, group style changes and functionality changes into separate commits.
  * This way, functionality change commits are not cluttered by style changes, and style change commits can be more casually reviewed, knowing that there are no functional changes.
* When practical, group moving files and editing files into separate commits
  * Due to the way modern JavaScript imports usually contain relative paths, this point is less useful than it is for some other languages because moving JavaScript files usually results in changes to its import paths, making it rare that moving a JavaScript file does not also result in an edit.
* In general, branch names should be prefixed with either `feature/` or `bug/`
* PR branches should be free of TypeScript errors

## When Accepting a PR

* Squash merge any PR that has more than one commit