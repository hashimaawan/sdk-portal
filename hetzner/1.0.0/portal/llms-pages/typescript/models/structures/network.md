# Network

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRk5ldHdvcms

*This model accepts additional fields of type unknown.*


# Interface Name

`Network`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `created` | `string` | Required | Point in time when the Network was created (in ISO-8601 format) |
| `id` | `number` | Required | ID of the Network |
| `ipRange` | `string` | Required | IPv4 prefix of the whole Network |
| `labels` | `unknown` | Required | User-defined labels (key-value pairs) |
| `loadBalancers` | `number[] \| undefined` | Optional | Array of IDs of Load Balancers attached to this Network |
| `name` | `string` | Required | Name of the Network |
| `protection` | [`Protection11`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/protection-11.md) | Required | Protection configuration for the Network |
| `routes` | [`Route[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/route.md) | Required | Array of routes set in this Network |
| `servers` | `number[]` | Required | Array of IDs of Servers attached to this Network |
| `subnets` | [`Subnet[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/subnet.md) | Required | Array subnets allocated in this Network |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { Network, Type42 } from 'hetzner-cloud-apilib';

const network: Network = {
  created: '2016-01-30T23:50:00+00:00',
  id: 4711,
  ipRange: '10.0.0.0/16',
  labels: { 'key1': 'val1', 'key2': 'val2' },
  name: 'mynet',
  protection: {
    mDelete: false,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  routes: [
    {
      destination: '10.100.1.0/24',
      gateway: '10.0.1.1',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  servers: [
    42
  ],
  subnets: [
    {
      gateway: '10.0.0.1',
      networkZone: 'eu-central',
      type: Type42.Cloud,
      ipRange: '10.0.1.0/24',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  loadBalancers: [
    42
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



