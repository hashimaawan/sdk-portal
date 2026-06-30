# Server Types

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRlNlcnZlclR5cGVz

The Server types the Datacenter can handle


# Interface Name

`ServerTypes`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `available` | `number[]` | Required | IDs of Server types that are supported and for which the Datacenter has enough resources left |
| `availableForMigration` | `number[]` | Required | IDs of Server types that are supported and for which the Datacenter has enough resources left |
| `supported` | `number[]` | Required | IDs of Server types that are supported in the Datacenter |


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
};
```



