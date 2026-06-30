# Load Balancer Types Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VyJTI1MjBUeXBlcyUyNTIwUmVzcG9uc2Ux


# Interface Name

`LoadBalancerTypesResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `loadBalancerType` | [`LoadBalancerType \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/load-balancer-type.md) | Optional | - |


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
        },
        priceMonthly: {
          gross: 'gross2',
          net: 'net0',
        },
      },
      {
        location: 'location8',
        priceHourly: {
          gross: 'gross4',
          net: 'net2',
        },
        priceMonthly: {
          gross: 'gross2',
          net: 'net0',
        },
      },
      {
        location: 'location8',
        priceHourly: {
          gross: 'gross4',
          net: 'net2',
        },
        priceMonthly: {
          gross: 'gross2',
          net: 'net0',
        },
      }
    ],
  },
};
```



