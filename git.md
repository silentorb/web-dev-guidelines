# Git Workflow

## When Submitting a PR

* Commit messages should be meaningful and distinct
* Break large tasks into multiple PRs
* In general, branch names should be prefixed with either `feature/` or `bug/`
* PR branches should be free of TypeScript errors
* Repos for production backend or frontend code should be created with `prod`, `staging`, and `dev` branches and no `master` or `main` branch
  * Repos for libraries that are not directly deployed can use a `master` branch
* When a merged PR is squashed, developers need to be sure to promptly merge squashed merges back into their development branches or there will be history conflicts

## When Accepting a PR

* Squash merge any PR that has more than one commit