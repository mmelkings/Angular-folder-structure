
  
# MODELS

  
All the *models* are included here

A model represents a structure of data used. Our models help us for declare a type of specific data, which is going to replace the generic type *Object*
 

## How do you see a model?

```ts
export class User {
	constructor(
		public name: string,
		public email: string,
		public password: string,
		public role?: string,
		public _id?: string
	) {}
}

```

### How do I use?

```ts
import { User } from '../models/user.model';

export class ComponentExample implements OnInit{

	ngOnInit(){
		const user = new User(null, 'mail@mail.com', '123456');
	}
}

  

```