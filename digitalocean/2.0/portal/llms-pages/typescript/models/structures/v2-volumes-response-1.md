# V2 Volumes Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBWb2x1bWVzJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2VolumesResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `volume` | [`Volume \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/volume.md) | Optional | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { V2VolumesResponse1 } from 'digitalocean-apilib';

const v2VolumesResponse1: V2VolumesResponse1 = {
  volume: {
    createdAt: '2020-03-02T17:00:49Z',
    description: 'Block store for examples',
    dropletIds: [],
    id: '506f78a4-e098-11e5-ad9f-000f53306ae1',
    name: 'example',
    sizeGigabytes: 10,
    filesystemLabel: 'example',
    filesystemType: 'ext4',
    region: {
      available: true,
      features: [
        'private_networking',
        'backups',
        'ipv6',
        'metadata'
      ],
      name: 'New York 1',
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
      slug: 'nyc1',
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



