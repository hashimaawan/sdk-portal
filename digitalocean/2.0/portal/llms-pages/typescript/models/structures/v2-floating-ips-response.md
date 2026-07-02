# V2 Floating Ips Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBGbG9hdGluZyUyNTIwSXBzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2FloatingIpsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `floatingIps` | [`FloatingIp1[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/floating-ip-1.md) | Optional | - |
| `links` | [`Links \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/links.md) | Optional | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/meta.md) | Required | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { V2FloatingIpsResponse } from 'digitalocean-apilib';

const v2FloatingIpsResponse: V2FloatingIpsResponse = {
  meta: {
    total: 1,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  floatingIps: [
    {
      droplet: null,
      ip: '45.55.96.47',
      locked: false,
      projectId: '746c6152-2fa2-11ed-92d3-27aaa54e4988',
      region: {
        available: true,
        features: [
          'private_networking',
          'backups',
          'ipv6',
          'metadata',
          'install_agent',
          'storage',
          'image_transfer'
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
          's-32vcpu-192g'
        ],
        slug: 'nyc3',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
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



