# Price 7

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRlByaWNlNw


# Interface Name

`Price7`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `location` | `string` | Required | Name of the Location the price is for |
| `priceHourly` | [`PriceHourly6`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/price-hourly-6.md) | Required | Hourly costs for a Load Balancer type in this network zone |
| `priceMonthly` | [`PriceMonthly8`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/price-monthly-8.md) | Required | Monthly costs for a Load Balancer type in this network zone |


# Example

```ts
import { Price7 } from 'hetzner-cloud-apilib';

const price7: Price7 = {
  location: 'fsn1',
  priceHourly: {
    gross: '1.1900000000000000',
    net: '1.0000000000',
  },
  priceMonthly: {
    gross: '1.1900000000000000',
    net: '1.0000000000',
  },
};
```



