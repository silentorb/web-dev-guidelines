# Tech Startup Web Stack

## Common

* Node.js
* TypeScript
* Yarn 1
* ES Lint
* Dotenv

## Front End

* React
* Webpack
* Styled Components and/or MUI
  * MUI is a powerful but heavy solution
  * Styled Components are essential when styles are maintained in code
  * Styled Components are less important when using MUI
* Formik
* Redux (Minimal)
  * By default mostly store state in components and React Context
  * Use Redux for state that has a complex lifetime such as global state
* Redux Toolkit

## Back End

* NestJS
* PostgreSQL
* Basic REST
  * Don't worry about being 100% RESTful
  * 100% RESTful isn't practical
  * Most web APIs use a common subset of REST
* TypeORM
* Jest

## Dev Ops

* AWS
* RDS
* Cloudfront
* ECS
* CodePipeline