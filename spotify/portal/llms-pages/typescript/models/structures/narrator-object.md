# Narrator Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/typescript/x-redirect/JTI0bSUyRk5hcnJhdG9yT2JqZWN0

*This model accepts additional fields of type unknown.*


# Interface Name

`NarratorObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `string \| undefined` | Optional | The name of the Narrator. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  NarratorObject,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const narratorObject: NarratorObject = {
  name: 'name8',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



