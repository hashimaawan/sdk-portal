# Datacenter

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkRhdGFjZW50ZXI

*This model accepts additional fields of type unknown.*


# Interface Name

`Datacenter`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `description` | `string` | Required | Description of the Datacenter |
| `id` | `number` | Required | ID of the Resource |
| `location` | [`Location`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/location.md) | Required | - |
| `name` | `string` | Required | Unique identifier of the Datacenter |
| `serverTypes` | [`ServerTypes`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/server-types.md) | Required | The Server types the Datacenter can handle |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { Datacenter } from 'hetzner-cloud-apilib';

const datacenter: Datacenter = {
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
};
```



