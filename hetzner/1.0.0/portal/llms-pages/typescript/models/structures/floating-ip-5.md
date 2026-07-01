# Floating Ip 5

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkZsb2F0aW5nSXA1

*This model accepts additional fields of type unknown.*


# Interface Name

`FloatingIp5`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `prices` | [`Price6[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/price-6.md) | Required | Floating IP type costs per Location |
| `type` | [`Type48`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/enumerations/type-48.md) | Required | The type of the Floating IP |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { FloatingIp5, Type48 } from 'hetzner-cloud-apilib';

const floatingIp5: FloatingIp5 = {
  prices: [
    {
      location: 'fsn1',
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
  type: Type48.Ipv4,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



