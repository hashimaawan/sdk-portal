# Vault 3

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/typescript/x-redirect/JTI0bSUyRlZhdWx0Mw

*This model accepts additional fields of type unknown.*


# Interface Name

`Vault3`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `string \| undefined` | Optional | **Constraints**: *Pattern*: `^[\da-z]{26}$` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { Vault3 } from 'm-1-password-connectlib';

const vault3: Vault3 = {
  id: 'id0',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



