
#   Shared

  

All the shared-components are included here.

  

## What is considered a shared-component?

  

For the logic of this structure, we call " shared " a part of a view that is displayed in a page and it's more specific than a component but it's not have a route.

Examples:

* Headers
* Navbar of the website
* Footer

> Remember that a shared is a component with a specific functionality. Don't need Inputs or Outputs.

## How can I create a shared?

We create a shared like a component.
In our console we use the next command (on the app folder)


```bash

ng generate component sharedName

```

  
See the [Angular CLI Documentation ](https://angular.io/cli/generate) for more information.

  

### Next Steps...

  

If everything went well we have the next structure
```
$ tree
.
├── shared
│   └── shared-name
|		├── shared-name.html
|		├── shared-name.ts
|		├── shared-name.css
│   	└── shared-name.spec
```


## Shared Module

The shared contain a module which help us to organize.
When creating shared-components, they must be imported in this module **NOT IN THE MAIN ** because this module is the ** ONLY ** that is imported in the main module, this is the way they comunicate.
