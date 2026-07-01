# Image 3

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkltYWdlMw

The cost of Image per GB/month

*This model accepts additional fields of type unknown.*


# Interface Name

`Image3`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `pricePerGbMonth` | [`PricePerGbMonth`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/price-per-gb-month.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { Image3 } from 'hetzner-cloud-apilib';

const image3: Image3 = {
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



