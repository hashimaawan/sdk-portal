# Load Balancer Types Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VyJTI1MjBUeXBlcyUyNTIwUmVzcG9uc2Ux

*This model accepts additional fields of type unknown.*


# Interface Name

`LoadBalancerTypesResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `loadBalancerType` | [`LoadBalancerType \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/load-balancer-type.md) | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { LoadBalancerTypesResponse1 } from 'hetzner-cloud-apilib';

const loadBalancerTypesResponse1: LoadBalancerTypesResponse1 = {
  loadBalancerType: {
    deprecated: 'deprecated2',
    description: 'description4',
    id: 205.06,
    maxAssignedCertificates: 211.64,
    maxConnections: 136.32,
    maxServices: 199.18,
    maxTargets: 152.52,
    name: 'name6',
    prices: [
      {
        location: 'location8',
        priceHourly: {
          gross: 'gross4',
          net: 'net2',
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        priceMonthly: {
          gross: 'gross2',
          net: 'net0',
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      {
        location: 'location8',
        priceHourly: {
          gross: 'gross4',
          net: 'net2',
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        priceMonthly: {
          gross: 'gross2',
          net: 'net0',
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      {
        location: 'location8',
        priceHourly: {
          gross: 'gross4',
          net: 'net2',
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        priceMonthly: {
          gross: 'gross2',
          net: 'net0',
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
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



