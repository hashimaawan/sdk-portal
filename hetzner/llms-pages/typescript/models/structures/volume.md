# Volume

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRlZvbHVtZQ

The cost of Volume per GB/month


# Interface Name

`Volume`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `pricePerGbMonth` | [`PricePerGbMonth`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/price-per-gb-month.md) | Required | - |


# Example

```ts
import { Volume } from 'hetzner-cloud-apilib';

const volume: Volume = {
  pricePerGbMonth: {
    gross: '1.1900000000000000',
    net: '1.0000000000',
  },
};
```



