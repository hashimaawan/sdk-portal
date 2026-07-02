# V2 Vpcs Members Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBWcGNzJTI1MjBNZW1iZXJzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2VpcsMembersResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `members` | [`Member[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/member.md) | Optional | - |
| `links` | [`Links \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/links.md) | Optional | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/meta.md) | Required | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { V2VpcsMembersResponse } from 'digitalocean-apilib';

const v2VpcsMembersResponse: V2VpcsMembersResponse = {
  meta: {
    total: 4,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  members: [
    {
      createdAt: '2020-03-13T19:30:48Z',
      name: 'nyc1-load-balancer-01',
      urn: 'do:loadbalancer:fb294d78-d193-4cb2-8737-ea620993591b',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      createdAt: '2020-03-13T19:30:18Z',
      name: 'db-postgresql-nyc1-55986',
      urn: 'do:dbaas:13f7a2f6-43df-4c4a-8129-8733267ddeea',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      createdAt: '2020-03-13T19:30:16Z',
      name: 'k8s-nyc1-1584127772221',
      urn: 'do:kubernetes:da39d893-96e1-4e4d-971d-1fdda33a46b1',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      createdAt: '2020-03-13T19:29:20Z',
      name: 'ubuntu-s-1vcpu-1gb-nyc1-01',
      urn: 'do:droplet:86e29982-03a7-4946-8a07-a0114dff8754',
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



