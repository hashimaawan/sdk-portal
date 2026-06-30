# Price 8

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRlByaWNlOA


# Interface Name

`Price8`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `location` | `string` | Required | Name of the Location the price is for |
| `priceHourly` | [`PriceHourly7`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/price-hourly-7.md) | Required | Hourly costs for a Primary IP type in this Location |
| `priceMonthly` | [`PriceMonthly9`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/price-monthly-9.md) | Required | Monthly costs for a Primary IP type in this Location |


# Example

```ts
import { Price8 } from 'hetzner-cloud-apilib';

const price8: Price8 = {
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



