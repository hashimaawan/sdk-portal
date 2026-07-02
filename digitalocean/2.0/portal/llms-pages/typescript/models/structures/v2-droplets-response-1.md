# V2 Droplets Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBEcm9wbGV0cyUyNTIwUmVzcG9uc2Ux

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2DropletsResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `droplet` | [`Droplet \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/droplet.md) | Optional | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import {
  Distribution,
  Status8,
  Type10,
  Type11,
  V2DropletsResponse1,
} from 'digitalocean-apilib';

const v2DropletsResponse1: V2DropletsResponse1 = {
  droplet: {
    backupIds: [
      156,
      157,
      158
    ],
    createdAt: '2016-03-13T12:52:32.123Z',
    disk: 150,
    features: [
      'features1'
    ],
    id: 28,
    image: {
      createdAt: '2016-03-13T12:52:32.123Z',
      description: 'description6',
      distribution: Distribution.CoreOs,
      errorMessage: 'error_message8',
      id: 128,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    locked: false,
    memory: 64,
    name: 'name0',
    networks: {
      v4: [
        {
          gateway: 'gateway2',
          ipAddress: 'ip_address2',
          netmask: 'netmask2',
          type: Type10.Public,
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        {
          gateway: 'gateway2',
          ipAddress: 'ip_address2',
          netmask: 'netmask2',
          type: Type10.Public,
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        {
          gateway: 'gateway2',
          ipAddress: 'ip_address2',
          netmask: 'netmask2',
          type: Type10.Public,
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        }
      ],
      v6: [
        {
          gateway: 'gateway4',
          ipAddress: 'ip_address4',
          netmask: 106,
          type: Type11.Public,
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        {
          gateway: 'gateway4',
          ipAddress: 'ip_address4',
          netmask: 106,
          type: Type11.Public,
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        }
      ],
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    nextBackupWindow: {
      end: '2016-03-13T12:52:32.123Z',
      start: '2016-03-13T12:52:32.123Z',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    region: {
      available: false,
      features: [
        'features7',
        'features8',
        'features9'
      ],
      name: 'name6',
      sizes: [
        'sizes6'
      ],
      slug: 'slug0',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    size: {
      available: false,
      description: 'description0',
      disk: 252,
      memory: 168,
      priceHourly: 121.04,
      priceMonthly: 162.04,
      regions: [
        'regions5'
      ],
      slug: 'slug6',
      transfer: 150.78,
      vcpus: 234,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    sizeSlug: 'size_slug0',
    snapshotIds: [
      145,
      146,
      147
    ],
    status: Status8.New,
    tags: [
      'tags5',
      'tags6'
    ],
    vcpus: 132,
    volumeIds: [
      'volume_ids0'
    ],
    kernel: {
      id: 16,
      name: 'name4',
      version: 'version0',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    vpcUuid: 'vpc_uuid0',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



