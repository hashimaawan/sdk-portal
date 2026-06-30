# Datacenter 6

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRkRhdGFjZW50ZXI2

Datacenter this Resource is located at


# Interface Name

`Datacenter6`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `description` | `string` | Required | Description of the Datacenter |
| `id` | `number` | Required | ID of the Resource |
| `location` | [`Location`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/location.md) | Required | - |
| `name` | `string` | Required | Unique identifier of the Datacenter |
| `serverTypes` | [`ServerTypes`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/server-types.md) | Required | The Server types the Datacenter can handle |


# Example

```ts
import { Datacenter6 } from 'hetzner-cloud-apilib';

const datacenter6: Datacenter6 = {
  description: 'Falkenstein DC Park 8',
  id: 42,
  location: {
    city: 'Falkenstein',
    country: 'DE',
    description: 'Falkenstein DC Park 1',
    id: 1,
    latitude: 50.47612,
    longitude: 12.370071,
    name: 'fsn1',
    networkZone: 'eu-central',
  },
  name: 'fsn1-dc8',
  serverTypes: {
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
  },
};
```



