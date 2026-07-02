# V2 Droplets Snapshots Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBEcm9wbGV0cyUyNTIwU25hcHNob3RzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2DropletsSnapshotsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `snapshots` | [`Backup1[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/backup-1.md) | Optional | - |
| `links` | [`Links \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/links.md) | Optional | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/meta.md) | Required | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Type13, V2DropletsSnapshotsResponse } from 'digitalocean-apilib';

const v2DropletsSnapshotsResponse: V2DropletsSnapshotsResponse = {
  meta: {
    total: 1,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  snapshots: [
    {
      id: 66,
      createdAt: '2016-03-13T12:52:32.123Z',
      minDiskSize: 112,
      name: 'name2',
      regions: [
        'regions7',
        'regions8'
      ],
      sizeGigabytes: 148.48,
      type: Type13.Snapshot,
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



