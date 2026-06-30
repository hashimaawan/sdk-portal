# Price 6

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRlByaWNlNg


# Interface Name

`Price6`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `location` | `string` | Required | Name of the Location the price is for |
| `priceMonthly` | [`PriceMonthly7`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/price-monthly-7.md) | Required | Monthly costs for a Floating IP type in this Location |


# Example

```ts
import { Price6 } from 'hetzner-cloud-apilib';

const price6: Price6 = {
  location: 'fsn1',
  priceMonthly: {
    gross: '1.1900000000000000',
    net: '1.0000000000',
  },
};
```



