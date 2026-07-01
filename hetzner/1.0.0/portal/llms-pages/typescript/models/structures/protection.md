# Protection

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlByb3RlY3Rpb24

Protection configuration for the Resource

*This model accepts additional fields of type unknown.*


# Interface Name

`Protection`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `mDelete` | `boolean` | Required | If true, prevents the Resource from being deleted |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { Protection } from 'hetzner-cloud-apilib';

const protection: Protection = {
  mDelete: false,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



