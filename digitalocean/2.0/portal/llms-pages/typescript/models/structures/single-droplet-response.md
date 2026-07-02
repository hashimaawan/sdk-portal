# Single Droplet Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlNpbmdsZSUyNTIwRHJvcGxldCUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`SingleDropletResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `droplet` | [`Droplet`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/droplet.md) | Required | - |
| `links` | [`Links1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/links-1.md) | Required | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import {
  Distribution,
  Region2,
  SingleDropletResponse,
  Status7,
  Status8,
  Type10,
  Type11,
  Type9,
} from 'digitalocean-apilib';

const singleDropletResponse: SingleDropletResponse = {
  droplet: {
    backupIds: [
      53893572
    ],
    createdAt: '2020-07-21T18:37:44Z',
    disk: 25,
    features: [
      'backups',
      'private_networking',
      'ipv6'
    ],
    id: 3164444,
    image: {
      createdAt: '2020-05-04T22:23:02Z',
      description: 'description6',
      distribution: Distribution.Ubuntu,
      errorMessage: 'error_message8',
      id: 7555620,
      minDiskSize: 20,
      name: 'Nifty New Snapshot',
      mPublic: true,
      regions: [
        Region2.Nyc1,
        Region2.Nyc2
      ],
      sizeGigabytes: 2.34,
      slug: 'nifty1',
      status: Status7.New,
      tags: [
        'base-image',
        'prod'
      ],
      type: Type9.Snapshot,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    locked: false,
    memory: 1024,
    name: 'example.com',
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
      end: '2019-12-04T23:00:00Z',
      start: '2019-12-04T00:00:00Z',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
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
    size: {
      available: true,
      description: 'Basic',
      disk: 25,
      memory: 1024,
      priceHourly: 0.00743999984115362,
      priceMonthly: 5,
      regions: [
        'ams2',
        'ams3',
        'blr1',
        'fra1',
        'lon1',
        'nyc1',
        'nyc2',
        'nyc3',
        'sfo1',
        'sfo2',
        'sfo3',
        'sgp1',
        'tor1'
      ],
      slug: 's-1vcpu-1gb',
      transfer: 1,
      vcpus: 1,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    sizeSlug: 's-1vcpu-1gb',
    snapshotIds: [
      67512819
    ],
    status: Status8.Active,
    tags: [
      'web',
      'env:prod'
    ],
    vcpus: 1,
    volumeIds: [
      '506f78a4-e098-11e5-ad9f-000f53306ae1'
    ],
    kernel: {
      id: 16,
      name: 'name4',
      version: 'version0',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    vpcUuid: '760e09ef-dc84-11e8-981e-3cfdfeaae000',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  links: {
    actions: [
      {
        href: 'href0',
        id: 154,
        rel: 'rel4',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      }
    ],
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



