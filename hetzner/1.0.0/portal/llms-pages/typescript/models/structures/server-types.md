# Server Types

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlNlcnZlclR5cGVz

The Server types the Datacenter can handle

*This model accepts additional fields of type unknown.*


# Interface Name

`ServerTypes`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `available` | `number[]` | Required | IDs of Server types that are supported and for which the Datacenter has enough resources left |
| `availableForMigration` | `number[]` | Required | IDs of Server types that are supported and for which the Datacenter has enough resources left |
| `supported` | `number[]` | Required | IDs of Server types that are supported in the Datacenter |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { ServerTypes } from 'hetzner-cloud-apilib';

const serverTypes: ServerTypes = {
  available: [
    1,
    2,
    3
  ],
  availableForMigration: [
    1,
    2,
    3
  ],
  supported: [
    1,
    2,
    3
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



