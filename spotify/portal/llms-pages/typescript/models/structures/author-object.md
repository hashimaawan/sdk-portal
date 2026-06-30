# Author Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/typescript/x-redirect/JTI0bSUyRkF1dGhvck9iamVjdA

*This model accepts additional fields of type unknown.*


# Interface Name

`AuthorObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `string \| undefined` | Optional | The name of the author. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  AuthorObject,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const authorObject: AuthorObject = {
  name: 'name4',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



