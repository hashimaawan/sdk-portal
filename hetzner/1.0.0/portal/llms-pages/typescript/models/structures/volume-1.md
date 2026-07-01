# Volume 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlZvbHVtZTE


# Interface Name

`Volume1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `created` | `string` | Required | Point in time when the Resource was created (in ISO-8601 format) |
| `format` | `string \| null` | Required | Filesystem of the Volume if formatted on creation, null if not formatted on creation |
| `id` | `number` | Required | ID of the Resource |
| `labels` | `Record<string, string>` | Required | User-defined labels (key-value pairs) |
| `linuxDevice` | `string` | Required | Device path on the file system for the Volume |
| `location` | [`Location16`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/location-16.md) | Required | Location of the Volume. Volume can only be attached to Servers in the same Location. |
| `name` | `string` | Required | Name of the Resource. Must be unique per Project. |
| `protection` | [`Protection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/protection.md) | Required | Protection configuration for the Resource |
| `server` | `number \| null` | Required | ID of the Server the Volume is attached to, null if it is not attached at all |
| `size` | `number` | Required | Size in GB of the Volume |
| `status` | [`Status113Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/enumerations/status-113.md) | Required | Current status of the Volume |


# Example

```ts
import { Status113Enum, Volume1 } from 'hetzner-cloud-apilib';

const volume1: Volume1 = {
  created: '2016-01-30T23:55:00+00:00',
  format: 'xfs',
  id: 42,
  labels: {
    'key0': 'labels8'
  },
  linuxDevice: '/dev/disk/by-id/scsi-0HC_Volume_4711',
  location: {
    city: 'Falkenstein',
    country: 'DE',
    description: 'Falkenstein DC Park 1',
    id: 1,
    latitude: 50.47612,
    longitude: 12.370071,
    name: 'fsn1',
    networkZone: 'eu-central',
  },
  name: 'my-resource',
  protection: {
    mDelete: false,
  },
  server: 12,
  size: 42,
  status: Status113Enum.Available,
};
```



