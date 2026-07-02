# V2 Snapshots Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBTbmFwc2hvdHMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2SnapshotsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `snapshots` | [`Snapshot[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/snapshot.md) | Optional | - |
| `links` | [`Links \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/links.md) | Optional | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/meta.md) | Required | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { ResourceType1, V2SnapshotsResponse } from 'digitalocean-apilib';

const v2SnapshotsResponse: V2SnapshotsResponse = {
  meta: {
    total: 1,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  snapshots: [
    {
      id: 'id2',
      createdAt: '2016-03-13T12:52:32.123Z',
      minDiskSize: 112,
      name: 'name2',
      regions: [
        'regions7',
        'regions8'
      ],
      sizeGigabytes: 148.48,
      resourceId: 'resource_id8',
      resourceType: ResourceType1.Droplet,
      tags: [
        'tags7',
        'tags8',
        'tags9'
      ],
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      id: 'id2',
      createdAt: '2016-03-13T12:52:32.123Z',
      minDiskSize: 112,
      name: 'name2',
      regions: [
        'regions7',
        'regions8'
      ],
      sizeGigabytes: 148.48,
      resourceId: 'resource_id8',
      resourceType: ResourceType1.Droplet,
      tags: [
        'tags7',
        'tags8',
        'tags9'
      ],
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      id: 'id2',
      createdAt: '2016-03-13T12:52:32.123Z',
      minDiskSize: 112,
      name: 'name2',
      regions: [
        'regions7',
        'regions8'
      ],
      sizeGigabytes: 148.48,
      resourceId: 'resource_id8',
      resourceType: ResourceType1.Droplet,
      tags: [
        'tags7',
        'tags8',
        'tags9'
      ],
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



