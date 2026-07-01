# Floating Ip 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkZsb2F0aW5nSXA0

The cost of one Floating IP per month


# Interface Name

`FloatingIp4`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `priceMonthly` | [`PriceMonthly6`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/price-monthly-6.md) | Required | - |


# Example

```ts
import { FloatingIp4 } from 'hetzner-cloud-apilib';

const floatingIp4: FloatingIp4 = {
  priceMonthly: {
    gross: '1.1900000000000000',
    net: '1.0000000000',
  },
};
```



