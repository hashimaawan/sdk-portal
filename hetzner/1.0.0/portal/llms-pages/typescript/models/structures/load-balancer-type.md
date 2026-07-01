# Load Balancer Type

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclR5cGU

*This model accepts additional fields of type unknown.*


# Interface Name

`LoadBalancerType`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deprecated` | `string \| null` | Required | Point in time when the Load Balancer type is deprecated (in ISO-8601 format) |
| `description` | `string` | Required | Description of the Load Balancer type |
| `id` | `number` | Required | ID of the Load Balancer type |
| `maxAssignedCertificates` | `number` | Required | Number of SSL Certificates that can be assigned to a single Load Balancer |
| `maxConnections` | `number` | Required | Number of maximum simultaneous open connections |
| `maxServices` | `number` | Required | Number of services a Load Balancer of this type can have |
| `maxTargets` | `number` | Required | Number of targets a single Load Balancer can have |
| `name` | `string` | Required | Unique identifier of the Load Balancer type |
| `prices` | [`Price[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/price.md) | Required | Prices in different network zones |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { LoadBalancerType } from 'hetzner-cloud-apilib';

const loadBalancerType: LoadBalancerType = {
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
};
```



