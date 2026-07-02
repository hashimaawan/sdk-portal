# V2 Volumes Request 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBWb2x1bWVzJTI1MjBSZXF1ZXN0MQ

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2VolumesRequest1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `createdAt` | `string \| undefined` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the block storage volume was created. |
| `description` | `string \| undefined` | Optional | An optional free-form text field to describe a block storage volume. |
| `dropletIds` | `number[] \| null \| undefined` | Optional, Read-only | An array containing the IDs of the Droplets the volume is attached to. Note that at this time, a volume can only be attached to a single Droplet. |
| `id` | `string \| undefined` | Optional, Read-only | The unique identifier for the block storage volume. |
| `name` | `string` | Required | A human-readable name for the block storage volume. Must be lowercase and be composed only of numbers, letters and "-", up to a limit of 64 characters. The name must begin with a letter. |
| `sizeGigabytes` | `number` | Required | The size of the block storage volume in GiB (1024^3). |
| `tags` | `string[] \| null \| undefined` | Optional | A flat array of tag names as strings to be applied to the resource. Tag names may be for either existing or new tags. |
| `snapshotId` | `string \| undefined` | Optional | The unique identifier for the volume snapshot from which to create the volume. |
| `filesystemType` | `string \| undefined` | Optional | The name of the filesystem type to be used on the volume. When provided, the volume will automatically be formatted to the specified filesystem type. Currently, the available options are `ext4` and `xfs`. Pre-formatted volumes are automatically mounted when attached to Ubuntu, Debian, Fedora, Fedora Atomic, and CentOS Droplets created on or after April 26, 2018. Attaching pre-formatted volumes to other Droplets is not recommended. |
| `filesystemLabel` | `string \| undefined` | Optional | **Constraints**: *Maximum Length*: `12` |
| `region` | [`Region2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/region-2.md) | Required | The slug identifier for the region where the resource will initially be  available. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Region2, V2VolumesRequest1 } from 'digitalocean-apilib';

const v2VolumesRequest1: V2VolumesRequest1 = {
  name: 'example',
  sizeGigabytes: 10,
  region: Region2.Nyc3,
  createdAt: '2020-03-02T17:00:49Z',
  description: 'Block store for examples',
  dropletIds: [],
  id: '506f78a4-e098-11e5-ad9f-000f53306ae1',
  tags: [
    'base-image',
    'prod'
  ],
  snapshotId: 'b0798135-fb76-11eb-946a-0a58ac146f33',
  filesystemType: 'ext4',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



