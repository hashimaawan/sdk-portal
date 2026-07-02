# Volume

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlZvbHVtZQ

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Volume`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `createdAt` | `string \| undefined` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the block storage volume was created. |
| `description` | `string \| undefined` | Optional | An optional free-form text field to describe a block storage volume. |
| `dropletIds` | `number[] \| null \| undefined` | Optional, Read-only | An array containing the IDs of the Droplets the volume is attached to. Note that at this time, a volume can only be attached to a single Droplet. |
| `id` | `string \| undefined` | Optional, Read-only | The unique identifier for the block storage volume. |
| `name` | `string \| undefined` | Optional | A human-readable name for the block storage volume. Must be lowercase and be composed only of numbers, letters and "-", up to a limit of 64 characters. The name must begin with a letter. |
| `sizeGigabytes` | `number \| undefined` | Optional | The size of the block storage volume in GiB (1024^3). |
| `tags` | `string[] \| null \| undefined` | Optional | A flat array of tag names as strings to be applied to the resource. Tag names may be for either existing or new tags. |
| `filesystemLabel` | `string \| undefined` | Optional | The label currently applied to the filesystem. |
| `filesystemType` | `string \| undefined` | Optional | The type of filesystem currently in-use on the volume. |
| `region` | [`Region \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/region.md) | Optional, Read-only | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Volume } from 'digitalocean-apilib';

const volume: Volume = {
  createdAt: '2020-03-02T17:00:49Z',
  description: 'Block store for examples',
  dropletIds: [],
  id: '506f78a4-e098-11e5-ad9f-000f53306ae1',
  name: 'example',
  sizeGigabytes: 10,
  tags: [
    'base-image',
    'prod'
  ],
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
};
```



