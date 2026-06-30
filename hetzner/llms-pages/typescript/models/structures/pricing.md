# Pricing

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRlByaWNpbmc


# Interface Name

`Pricing`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `currency` | `string` | Required | Currency the returned prices are expressed in, coded according to ISO 4217 |
| `floatingIp` | [`FloatingIp4`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/floating-ip-4.md) | Required | The cost of one Floating IP per month |
| `floatingIps` | [`FloatingIp5[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/floating-ip-5.md) | Required | Costs of Floating IPs types per Location and type |
| `image` | [`Image3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/image-3.md) | Required | The cost of Image per GB/month |
| `loadBalancerTypes` | [`LoadBalancerType6[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/load-balancer-type-6.md) | Required | Costs of Load Balancer types per Location and type |
| `primaryIps` | [`PrimaryIp[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/primary-ip.md) | Required | Costs of Primary IPs types per Location |
| `serverBackup` | [`ServerBackup`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/server-backup.md) | Required | Will increase base Server costs by specific percentage |
| `serverTypes` | [`ServerTypes2[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/server-types-2.md) | Required | Costs of Server types per Location and type |
| `traffic` | [`Traffic`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/traffic.md) | Required | The cost of additional traffic per TB |
| `vatRate` | `string` | Required | The VAT rate used for calculating prices with VAT |
| `volume` | [`Volume`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/volume.md) | Required | The cost of Volume per GB/month |


# Example

```ts
import { Pricing, Type48Enum, Type49Enum } from 'hetzner-cloud-apilib';

const pricing: Pricing = {
  currency: 'EUR',
  floatingIp: {
    priceMonthly: {
      gross: '1.1900000000000000',
      net: '1.0000000000',
    },
  },
  floatingIps: [
    {
      prices: [
        {
          location: 'fsn1',
          priceMonthly: {
            gross: '1.1900000000000000',
            net: '1.0000000000',
          },
        }
      ],
      type: Type48Enum.Ipv4,
    }
  ],
  image: {
    pricePerGbMonth: {
      gross: '1.1900000000000000',
      net: '1.0000000000',
    },
  },
  loadBalancerTypes: [
    {
      id: 1,
      name: 'lb11',
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
    }
  ],
  primaryIps: [
    {
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
    }
  ],
  serverBackup: {
    percentage: '20.0000000000',
  },
  serverTypes: [
    {
      id: 4,
      name: 'cx11',
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
    }
  ],
  traffic: {
    pricePerTb: {
      gross: '1.1900000000000000',
      net: '1.0000000000',
    },
  },
  vatRate: '19.000000',
  volume: {
    pricePerGbMonth: {
      gross: '1.1900000000000000',
      net: '1.0000000000',
    },
  },
};
```



