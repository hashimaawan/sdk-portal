# Server Types 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlNlcnZlclR5cGVzMg

*This model accepts additional fields of type unknown.*


# Interface Name

`ServerTypes2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `number` | Required | ID of the Server type the price is for |
| `name` | `string` | Required | Name of the Server type the price is for |
| `prices` | [`Price9[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/price-9.md) | Required | Server type costs per Location |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { ServerTypes2 } from 'hetzner-cloud-apilib';

const serverTypes2: ServerTypes2 = {
  id: 4,
  name: 'cx11',
  prices: [
    {
      location: 'fsn1',
      priceHourly: {
        gross: '1.1900000000000000',
        net: '1.0000000000',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      priceMonthly: {
        gross: '1.1900000000000000',
        net: '1.0000000000',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



