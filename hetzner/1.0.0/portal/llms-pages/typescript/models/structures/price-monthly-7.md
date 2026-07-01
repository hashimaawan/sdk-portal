# Price Monthly 7

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlByaWNlTW9udGhseTc

Monthly costs for a Floating IP type in this Location

*This model accepts additional fields of type unknown.*


# Interface Name

`PriceMonthly7`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `gross` | `string` | Required | Price with VAT added |
| `net` | `string` | Required | Price without VAT |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { PriceMonthly7 } from 'hetzner-cloud-apilib';

const priceMonthly7: PriceMonthly7 = {
  gross: '1.1900000000000000',
  net: '1.0000000000',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



