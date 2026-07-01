# Traffic

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlRyYWZmaWM

The cost of additional traffic per TB

*This model accepts additional fields of type unknown.*


# Interface Name

`Traffic`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `pricePerTb` | [`PricePerTb`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/price-per-tb.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { Traffic } from 'hetzner-cloud-apilib';

const traffic: Traffic = {
  pricePerTb: {
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



