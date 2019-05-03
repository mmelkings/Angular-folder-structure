
  

# Constants

 All the constants that we use on the project are included here
* Url's
* API key
* Enum
* Roles
* Index

## How can I create a constant?

The constants are basically an export class that are imported into our project. We can create some .ts files depending on the purpose.

  
### Example

```ts

export class AppConstants {
	public static URL='http://127.0.0.0/myApi';
}

```

For use it:

```ts
import { AppConstants } from '../constants/appConstants';
...

let url = AppConstants.URL;

```