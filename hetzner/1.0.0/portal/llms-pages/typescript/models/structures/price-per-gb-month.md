# Price per Gb Month

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlByaWNlUGVyR2JNb250aA


# Interface Name

`PricePerGbMonth`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `gross` | `string` | Required | Price with VAT added |
| `net` | `string` | Required | Price without VAT |


# Example

```ts
import { PricePerGbMonth } from 'hetzner-cloud-apilib';

const pricePerGbMonth: PricePerGbMonth = {
  gross: '1.1900000000000000',
  net: '1.0000000000',
};
```



