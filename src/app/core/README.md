
  

# CORE

In the folder ***core*** are all our services.
Any communication with the **backend** or anyone API happens here.
It can contain the following functionalities:

* authentication
* services
* guards
* interceptors
* utils


## How Can I create a Service?

In the console we use de next command

```bash
ng generate service loginAuthentication
```

See the [Angular CLI Documentation ](https://angular.io/cli/generate) for more information.


## Core Module and  Core Index

The **core** contains a module and a index, which help us to organize and export the services to the components and pages.

When creating services, they must be imported in this module **NOT IN THE MAIN** because this module is the  **ONLY**  that is imported in the main module, this is the way they communicate.

### How do I import a Service?

1. First you must export since the **index.ts** of the core, in this way, when wanting to call it somewhere else, we call this instead of the original. It helps when whe have to much services and it's annoyinh to call each of different path.
  
```ts
export {AuthenticationLoginService}  from'./auth/authenticationLogin.service';
```

> Remember that it is just an example..

2. If you already create a service you must make sure that it has been imported correctly in ***core.module.ts***.

```ts
import { AuthenticationLoginService } from './core.index';
@NgModule({
	imports: [ ... ],
	providers: [
	AuthenticationLoginService
],
declarations: [...]
})

export class CoreModule { }

```

> In this way it's already imported into out project and it can be called in anywhere.

  
### ¿How do I use?

```ts
import { AuthenticationLoginService } from '../../core/core.index';

export class ComponentExample implements OnInit{

	constructor( public _auth: AuthenticationLoginService ){}
	
	ngOnInit(){
		let token = this._auth.getToken();
	}

}

  

```