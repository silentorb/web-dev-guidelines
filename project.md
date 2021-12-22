# Project Structure

## Configuration

* Any configuration files intended to be modified for deployment should not be tracked by Git
  * Their paths should be added to `.gitignore`

## Development

* A project only needs to run on Linux for production, but should support Linux, Mac, and Windows for local development

* A project that cannot be run and tested locally (with at least fake services) should be considered broken and not ready for production use

* Do not track IDE specific files in Git

## Code

* Source code files should not be in the root folder of a project

* There should be no IP addresses or URLs in source code

* There should be no port numbers in source code except as optional default values

## Architecture

* Client and server projects should be stored in separate repositories

* Client projects should not directly depend on server projects and vice versa

### Node.js

* Always lock dependencies to a major version using either exact versions or the caret symbol

  * Very good: "2.0.1"

  * Good: "^2.0.1"

  * Bad: ">=2.0.1"

  * Very bad: "*"