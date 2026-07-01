# Price 9

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlByaWNlOQ


# Interface Name

`Price9`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `location` | `string` | Required | Name of the Location the price is for |
| `priceHourly` | [`PriceHourly8`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/price-hourly-8.md) | Required | Hourly costs for a Server type in this Location |
| `priceMonthly` | [`PriceMonthly10`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/price-monthly-10.md) | Required | Monthly costs for a Server type in this Location |


# Example

```ts
import { Price9 } from 'hetzner-cloud-apilib';

const price9: Price9 = {
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



