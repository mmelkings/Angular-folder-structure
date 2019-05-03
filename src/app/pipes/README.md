
# PIPES


All the *pipes* are included here.
A  **pipe** is a way to write display-value transformations that you can declare in your HTML.

## How is it created?
In our console we use the next command (on the app folder)

```bash
ng generate pipe pipeName
```

See the [Angular CLI Documentation ](https://angular.io/cli/generate) for more information.


### Next Steps...

 
If everything went well we have the next structure

```$ tree
├── pipes
│ └── pipe-name.ts
```

## Pipes Module

The pipes contain a module which help us to organize.

When creating pipes, they must be imported in this module **NOT IN THE MAIN**  because this module is the **ONLY**  that is imported in the main module, this is the way they communicate.