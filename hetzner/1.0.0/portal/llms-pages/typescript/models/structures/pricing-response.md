# Pricing Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlByaWNpbmclMjUyMFJlc3BvbnNl

*This model accepts additional fields of type unknown.*


# Interface Name

`PricingResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `pricing` | [`Pricing`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/pricing.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { PricingResponse, Type48, Type49 } from 'hetzner-cloud-apilib';

const pricingResponse: PricingResponse = {
  pricing: {
    currency: 'EUR',
    floatingIp: {
      priceMonthly: {
        gross: '1.1900000000000000',
        net: '1.0000000000',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
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
              additionalProperties: {
                'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
              },
            },
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          }
        ],
        type: Type48.Ipv4,
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      }
    ],
    image: {
      pricePerGbMonth: {
        gross: '1.1900000000000000',
        net: '1.0000000000',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
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
              additionalProperties: {
                'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
              },
            },
            priceMonthly: {
              gross: '1.1900000000000000',
              net: '1.0000000000',
              additionalProperties: {
                'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
              },
            },
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          }
        ],
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
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
              additionalProperties: {
                'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
              },
            },
            priceMonthly: {
              gross: '1.1900000000000000',
              net: '1.0000000000',
              additionalProperties: {
                'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
              },
            },
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          }
        ],
        type: Type49.Ipv4,
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      }
    ],
    serverBackup: {
      percentage: '20.0000000000',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
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
              additionalProperties: {
                'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
              },
            },
            priceMonthly: {
              gross: '1.1900000000000000',
              net: '1.0000000000',
              additionalProperties: {
                'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
              },
            },
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          }
        ],
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      }
    ],
    traffic: {
      pricePerTb: {
        gross: '1.1900000000000000',
        net: '1.0000000000',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    vatRate: '19.000000',
    volume: {
      pricePerGbMonth: {
        gross: '1.1900000000000000',
        net: '1.0000000000',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



