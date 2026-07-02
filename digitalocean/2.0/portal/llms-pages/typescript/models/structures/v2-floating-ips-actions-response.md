# V2 Floating Ips Actions Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBGbG9hdGluZyUyNTIwSXBzJTI1MjBBY3Rpb25zJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2FloatingIpsActionsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `actions` | [`Action[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/action.md) | Optional | - |
| `links` | [`Links \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/links.md) | Optional | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/meta.md) | Required | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Status1, V2FloatingIpsActionsResponse } from 'digitalocean-apilib';

const v2FloatingIpsActionsResponse: V2FloatingIpsActionsResponse = {
  meta: {
    total: 1,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  actions: [
    {
      completedAt: '2015-11-21T21:51:09Z',
      id: 72531856,
      region: {
        available: true,
        features: [
          'private_networking',
          'backups',
          'ipv6',
          'metadata'
        ],
        name: 'New York 3',
        sizes: [
          's-1vcpu-1gb',
          's-1vcpu-2gb',
          's-1vcpu-3gb',
          's-2vcpu-2gb',
          's-3vcpu-1gb',
          's-2vcpu-4gb',
          's-4vcpu-8gb',
          's-6vcpu-16gb',
          's-8vcpu-32gb',
          's-12vcpu-48gb',
          's-16vcpu-64gb',
          's-20vcpu-96gb',
          's-24vcpu-128gb',
          's-32vcpu-192gb'
        ],
        slug: 'nyc3',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      regionSlug: 'nyc3',
      resourceId: 758604197,
      resourceType: 'floating_ip',
      startedAt: '2015-11-21T21:51:09Z',
      status: Status1.Completed,
      type: 'reserve_ip',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  links: {
    pages: {
      last: 'last6',
      next: 'next2',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



