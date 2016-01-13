# Principles of Component Design

Components embrace the fact that fundamentally HTML, JS, CSS and images can not always describe a unit of functionality by themselves. Each bring different properties. Some
components can be described in terms of just one, some are mixtures. React
helps us define these components in a single way, the component.

## Current stack

* React
* CSS Modules
* File Loader

## Using modular CSS classes over components

Sometimes it is easier to write generic CSS classes that can be applied by
varying components. For example:

``` css
.patternBackground {
  background: url('./background.png');
}
```

``` javascript

import styles from "./backgrounds.css";

export default function Component (props) {
  return (
    <div className={style.patternBackground}></div>
  );
}

```

### What are we trying to achieve here?

* A single place to declare styles that can be referenced by multiple components
* A single place that can be updated as the application changes over time

## Exposing className vs wrapping in a container with style

When we expose className to be set by consumers of our components we are allowing all CSS properties to be set. This greatly increases the "API" surface area of the component and can lead to unexpected styling.

## Parallels to software development

### How can we embrace functional concepts?

## Premature Optimization

## Testing

* Making small components leads to easily testable code.

## Atomic Design

What are the levels of component design with respect to their intent. Single use, project specific, brand/company specific, universal reusable.


## Things that we do

* DRY
* Change one place, update many (normally app specific)
* Prototype, quick to realize ideas
