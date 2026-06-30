# Vault 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/typescript/x-redirect/JTI0bSUyRlZhdWx0MQ

*This model accepts additional fields of type unknown.*


# Interface Name

`Vault1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `string` | Required | **Constraints**: *Pattern*: `^[\da-z]{26}$` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { Vault1 } from 'm-1-password-connectlib';

const vault1: Vault1 = {
  id: 'id0',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



