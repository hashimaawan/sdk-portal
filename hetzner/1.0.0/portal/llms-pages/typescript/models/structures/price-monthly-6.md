# Price Monthly 6

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlByaWNlTW9udGhseTY


# Interface Name

`PriceMonthly6`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `gross` | `string` | Required | Price with VAT added |
| `net` | `string` | Required | Price without VAT |


# Example

```ts
import { PriceMonthly6 } from 'hetzner-cloud-apilib';

const priceMonthly6: PriceMonthly6 = {
  gross: '1.1900000000000000',
  net: '1.0000000000',
};
```



