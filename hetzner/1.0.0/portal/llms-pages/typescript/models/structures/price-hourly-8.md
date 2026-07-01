# Price Hourly 8

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlByaWNlSG91cmx5OA

Hourly costs for a Server type in this Location

*This model accepts additional fields of type unknown.*


# Interface Name

`PriceHourly8`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `gross` | `string` | Required | Price with VAT added |
| `net` | `string` | Required | Price without VAT |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { PriceHourly8 } from 'hetzner-cloud-apilib';

const priceHourly8: PriceHourly8 = {
  gross: '1.1900000000000000',
  net: '1.0000000000',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



