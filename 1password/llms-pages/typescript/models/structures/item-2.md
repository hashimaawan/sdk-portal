# Item 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/typescript/x-redirect/JTI0bSUyRkl0ZW0y

*This model accepts additional fields of type unknown.*


# Interface Name

`Item2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `string \| undefined` | Optional | **Constraints**: *Pattern*: `^[\da-z]{26}$` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { Item2 } from 'm-1-password-connectlib';

const item2: Item2 = {
  id: 'id2',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



