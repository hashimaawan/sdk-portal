# V2 Droplets Backups Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBEcm9wbGV0cyUyNTIwQmFja3VwcyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2DropletsBackupsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `backups` | [`Backup1[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/backup-1.md) | Optional | - |
| `links` | [`Links \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/links.md) | Optional | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/meta.md) | Required | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Type13, V2DropletsBackupsResponse } from 'digitalocean-apilib';

const v2DropletsBackupsResponse: V2DropletsBackupsResponse = {
  meta: {
    total: 1,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  backups: [
    {
      id: 196,
      createdAt: '2016-03-13T12:52:32.123Z',
      minDiskSize: 242,
      name: 'name4',
      regions: [
        'regions9',
        'regions0',
        'regions1'
      ],
      sizeGigabytes: 180.5,
      type: Type13.Snapshot,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      id: 196,
      createdAt: '2016-03-13T12:52:32.123Z',
      minDiskSize: 242,
      name: 'name4',
      regions: [
        'regions9',
        'regions0',
        'regions1'
      ],
      sizeGigabytes: 180.5,
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



