# Protection 20

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlByb3RlY3Rpb24yMA

Protection configuration for the Server

*This model accepts additional fields of type unknown.*


# Interface Name

`Protection20`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `mDelete` | `boolean` | Required | If true, prevents the Server from being deleted |
| `rebuild` | `boolean` | Required | If true, prevents the Server from being rebuilt |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { Protection20 } from 'hetzner-cloud-apilib';

const protection20: Protection20 = {
  mDelete: false,
  rebuild: false,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



