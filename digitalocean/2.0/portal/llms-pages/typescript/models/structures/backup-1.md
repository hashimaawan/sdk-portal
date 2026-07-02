# Backup 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkJhY2t1cDE

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Backup1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `number` | Required | The unique identifier for the snapshot or backup. |
| `createdAt` | `string` | Required | A time value given in ISO8601 combined date and time format that represents when the snapshot was created. |
| `minDiskSize` | `number` | Required | The minimum size in GB required for a volume or Droplet to use this snapshot. |
| `name` | `string` | Required | A human-readable name for the snapshot. |
| `regions` | `string[]` | Required | An array of the regions that the snapshot is available in. The regions are represented by their identifying slug values. |
| `sizeGigabytes` | `number` | Required | The billable size of the snapshot in gigabytes. |
| `type` | [`Type13`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/type-13.md) | Required | Describes the kind of image. It may be one of `snapshot` or `backup`. This specifies whether an image is a user-generated Droplet snapshot or automatically created Droplet backup. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Backup1, Type13 } from 'digitalocean-apilib';

const backup1: Backup1 = {
  id: 6372321,
  createdAt: '2020-07-28T16:47:44Z',
  minDiskSize: 25,
  name: 'web-01-1595954862243',
  regions: [
    'nyc3',
    'sfo3'
  ],
  sizeGigabytes: 2.34,
  type: Type13.Snapshot,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



