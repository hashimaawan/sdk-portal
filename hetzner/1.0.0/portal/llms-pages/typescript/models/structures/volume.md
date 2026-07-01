# Volume

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlZvbHVtZQ

The cost of Volume per GB/month

*This model accepts additional fields of type unknown.*


# Interface Name

`Volume`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `pricePerGbMonth` | [`PricePerGbMonth`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/price-per-gb-month.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { Volume } from 'hetzner-cloud-apilib';

const volume: Volume = {
  pricePerGbMonth: {
    gross: '1.1900000000000000',
    net: '1.0000000000',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



