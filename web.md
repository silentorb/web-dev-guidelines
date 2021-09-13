# Web App Development Guidelines

## Design

* The layout of a website should be as uniform across pages as possible
* Minimize the frequency of unique UI elements

## Styling

* Use styled components
* Avoid global styles other than the most universal of attributes such as font family
* Avoid global styles except for styling third-party components, which sometimes require cascading styling
* Minimize occurrences of the same line or block of CSS code.
* Group reoccurring CSS into styled component `css` blocks.
  * This improves static traceability
* Prefer composition over inheritance
* Minimize overriding style rules
  * The more rules are overridden, the harder it is to reason about styling pipelines, the more surprises and bugs occur, and the harder it is to tame and refactor existing styles

## React

* Use functions instead of classes to create React components
* Prefer shared styles over component-specific styles
* Include component-specific styling in the same file as the component
* Form field components should output refined data so that the form submission function needs to do as little cleanup of the form data as possible
  * Example: A field that only accepts numbers should store its field data as a number, not a string
* When expanding a component to be used in different cases, if possible split the component into smaller reusable components instead of adding configuration props to the component
  * Composition is flexible and infinitely scales, while increased configuration props creates traffic jams

