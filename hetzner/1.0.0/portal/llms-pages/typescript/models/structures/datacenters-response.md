# Datacenters Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkRhdGFjZW50ZXJzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type unknown.*


# Interface Name

`DatacentersResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `datacenters` | [`Datacenter[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/datacenter.md) | Required | - |
| `recommendation` | `number` | Required | The Datacenter which is recommended to be used to create new Servers. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { DatacentersResponse } from 'hetzner-cloud-apilib';

const datacentersResponse: DatacentersResponse = {
  datacenters: [
    {
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
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
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
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  recommendation: 1,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



