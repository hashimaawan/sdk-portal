# Pricing Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRlByaWNpbmclMjUyMFJlc3BvbnNl


# Interface Name

`PricingResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `pricing` | [`Pricing`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/pricing.md) | Required | - |


# Example

```ts
import {
  PricingResponse,
  Type48Enum,
  Type49Enum,
} from 'hetzner-cloud-apilib';

const pricingResponse: PricingResponse = {
  pricing: {
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
  },
};
```



