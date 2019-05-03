

# PAGES

All the *pages* are included here.

For the logic of ths structure a **page**  is a component that is not reused or injected somewhere, it show a interface.

## Examples:

* Dashboard
* Modules
* Product Views
* Complete forms

  
Do not confuse  **pages**  with **components**. On the pages we use the components, a component is, for example, a table. This component is used in a page where we inject the component and also add more functions of the page.
  
## How is it created?

In our console we use the next command (on the app folder)

```bash
ng generate component pageName
```

See the [Angular CLI Documentation ](https://angular.io/cli/generate) for more information.

### Next Steps...

If everything went well we have the next structure

```$ tree

├── pages
│ └── page-name
| ├── page-name.html
| ├── page-name.ts
| ├── page-name.css
│ └── page-name.spec
```

## Pages Module

The pages contain a module which help us to organize.

When creating pages, they must be imported in this module  **NOT IN THE MAIN** because this module is the  **ONLY**   that is imported in the main module, this is the way they communicate.
  
## Routing

We have a routes file (pages.routes.ts). In this file we have all the routing of our pages. It's an example:

```ts
const pagesRoutes: Routes = [
	{ path: 'dashboard', component: DashboardPage},
	{ path: 'products', component: ProductPage}
];
export const PAGES_ROUTES = RouterModule.forChild(pagesRoutes);
```

> It's important to export the constant like a `forChild` route, because it will be imported in the main routes (app.routes.ts)