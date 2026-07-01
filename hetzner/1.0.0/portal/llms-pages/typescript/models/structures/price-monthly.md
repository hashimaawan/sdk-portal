# Price Monthly

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlByaWNlTW9udGhseQ

Monthly costs for a Resource in this Location


# Interface Name

`PriceMonthly`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `gross` | `string` | Required | Price with VAT added |
| `net` | `string` | Required | Price without VAT |


# Example

```ts
import { PriceMonthly } from 'hetzner-cloud-apilib';

const priceMonthly: PriceMonthly = {
  gross: '1.1900000000000000',
  net: '1.0000000000',
};
```



