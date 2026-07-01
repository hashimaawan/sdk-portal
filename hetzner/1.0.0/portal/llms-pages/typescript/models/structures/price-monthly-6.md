# Price Monthly 6

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlByaWNlTW9udGhseTY

*This model accepts additional fields of type unknown.*


# Interface Name

`PriceMonthly6`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `gross` | `string` | Required | Price with VAT added |
| `net` | `string` | Required | Price without VAT |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { PriceMonthly6 } from 'hetzner-cloud-apilib';

const priceMonthly6: PriceMonthly6 = {
  gross: '1.1900000000000000',
  net: '1.0000000000',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



