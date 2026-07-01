# Primary Ip

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlByaW1hcnlJcA

*This model accepts additional fields of type unknown.*


# Interface Name

`PrimaryIp`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `prices` | [`Price8[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/price-8.md) | Required | Primary IP type costs per Location |
| `type` | [`Type49`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/enumerations/type-49.md) | Required | The type of the Primary IP |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { PrimaryIp, Type49 } from 'hetzner-cloud-apilib';

const primaryIp: PrimaryIp = {
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
  type: Type49.Ipv4,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



