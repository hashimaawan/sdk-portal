# Create Network Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkNyZWF0ZU5ldHdvcmtSZXF1ZXN0

*This model accepts additional fields of type unknown.*


# Interface Name

`CreateNetworkRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ipRange` | `string` | Required | IP range of the whole network which must span all included subnets. Must be one of the private IPv4 ranges of RFC1918. Minimum network size is /24. We highly recommend that you pick a larger network with a /16 netmask. |
| `labels` | [`Labels \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/labels.md) | Optional | User-defined labels (key-value pairs) |
| `name` | `string` | Required | Name of the network |
| `routes` | [`Route[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/route.md) | Optional | Array of routes set in this network. The destination of the route must be one of the private IPv4 ranges of RFC1918. The gateway must be a subnet/IP of the ip_range of the network object. The destination must not overlap with an existing ip_range in any subnets or with any destinations in other routes or with the first IP of the networks ip_range or with 172.31.1.1. The gateway cannot be the first IP of the networks ip_range and also cannot be 172.31.1.1. |
| `subnets` | [`Subnet1[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/subnet-1.md) | Optional | Array of subnets allocated. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { CreateNetworkRequest, Type42 } from 'hetzner-cloud-apilib';

const createNetworkRequest: CreateNetworkRequest = {
  ipRange: '10.0.0.0/16',
  name: 'mynet',
  labels: {
    labelkey: 'labelkey4',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  routes: [
    {
      destination: 'destination8',
      gateway: 'gateway6',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  subnets: [
    {
      networkZone: 'network_zone2',
      type: Type42.Cloud,
      ipRange: 'ip_range6',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      networkZone: 'network_zone2',
      type: Type42.Cloud,
      ipRange: 'ip_range6',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      networkZone: 'network_zone2',
      type: Type42.Cloud,
      ipRange: 'ip_range6',
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



