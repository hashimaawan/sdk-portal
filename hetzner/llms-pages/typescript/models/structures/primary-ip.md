# Primary Ip

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRlByaW1hcnlJcA


# Interface Name

`PrimaryIp`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `prices` | [`Price8[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/price-8.md) | Required | Primary IP type costs per Location |
| `type` | [`Type49Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/enumerations/type-49.md) | Required | The type of the Primary IP |


# Example

```ts
import { PrimaryIp, Type49Enum } from 'hetzner-cloud-apilib';

const primaryIp: PrimaryIp = {
  prices: [
    {
      location: 'fsn1',
      priceHourly: {
        gross: '1.1900000000000000',
        net: '1.0000000000',
      },
      priceMonthly: {
        gross: '1.1900000000000000',
        net: '1.0000000000',
      },
    }
  ],
  type: Type49Enum.Ipv4,
};
```



