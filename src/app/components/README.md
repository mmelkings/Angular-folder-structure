

  # Components

All the components are included here.


## What is considered a component?

For the logic of this structure, we call " component " a part of a view that is displayed on the screen, which is "reusable" anywhere on our pages. If a visual element is repeated in several places, it's necessary to create a component.

## How can I create a component?

In our console we use the next command (on the app folder)


```bash
ng generate component componentName
```
See the [Angular CLI Documentation ](https://angular.io/cli/generate) for more information.

### Next Steps...

If everything went well we have the next structure

```$ tree

├── components
│ └── component-name
| ├── component-name.html
| ├── component-name.ts
| ├── component-name.css
│ └── component-name.spec

```