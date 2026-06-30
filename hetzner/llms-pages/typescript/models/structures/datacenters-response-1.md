# Datacenters Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRkRhdGFjZW50ZXJzJTI1MjBSZXNwb25zZTE


# Interface Name

`DatacentersResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `datacenter` | [`Datacenter`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/datacenter.md) | Required | - |


# Example

```ts
import { DatacentersResponse1 } from 'hetzner-cloud-apilib';

const datacentersResponse1: DatacentersResponse1 = {
  datacenter: {
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
  },
};
```



