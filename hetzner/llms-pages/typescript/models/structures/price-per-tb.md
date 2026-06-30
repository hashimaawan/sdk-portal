# Price per Tb

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRlByaWNlUGVyVGI


# Interface Name

`PricePerTb`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `gross` | `string` | Required | Price with VAT added |
| `net` | `string` | Required | Price without VAT |


# Example

```ts
import { PricePerTb } from 'hetzner-cloud-apilib';

const pricePerTb: PricePerTb = {
  gross: '1.1900000000000000',
  net: '1.0000000000',
};
```



