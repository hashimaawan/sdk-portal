# Load Balancer Types Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VyJTI1MjBUeXBlcyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type unknown.*


# Interface Name

`LoadBalancerTypesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `loadBalancerTypes` | [`LoadBalancerType[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/load-balancer-type.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { LoadBalancerTypesResponse } from 'hetzner-cloud-apilib';

const loadBalancerTypesResponse: LoadBalancerTypesResponse = {
  loadBalancerTypes: [
    {
      deprecated: '2016-01-30T23:50:00+00:00',
      description: 'LB11',
      id: 1,
      maxAssignedCertificates: 10,
      maxConnections: 20000,
      maxServices: 5,
      maxTargets: 25,
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
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



