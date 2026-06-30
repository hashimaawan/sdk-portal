# Many Genres

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/typescript/x-redirect/JTI0bSUyRk1hbnlHZW5yZXM

*This model accepts additional fields of type unknown.*


# Interface Name

`ManyGenres`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `genres` | `string[]` | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  ManyGenres,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const manyGenres: ManyGenres = {
  genres: [
    'alternative',
    'samba'
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



