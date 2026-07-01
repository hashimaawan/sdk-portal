# Price

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlByaWNl


# Interface Name

`Price`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `location` | `string` | Required | Name of the Location the price is for |
| `priceHourly` | [`PriceHourly`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/price-hourly.md) | Required | Hourly costs for a Resource in this Location |
| `priceMonthly` | [`PriceMonthly`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/price-monthly.md) | Required | Monthly costs for a Resource in this Location |


# Example

```ts
import { Price } from 'hetzner-cloud-apilib';

const price: Price = {
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



