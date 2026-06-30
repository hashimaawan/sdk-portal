# Image

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRkltYWdl


# Interface Name

`Image`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `boundTo` | `number \| null` | Required | ID of Server the Image is bound to. Only set for Images of type `backup`. |
| `created` | `string` | Required | Point in time when the Resource was created (in ISO-8601 format) |
| `createdFrom` | [`CreatedFrom \| null`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/created-from.md) | Required | Information about the Server the Image was created from |
| `deleted` | `string \| null` | Required | Point in time where the Image was deleted (in ISO-8601 format) |
| `deprecated` | `string \| null` | Required | Point in time when the Image is considered to be deprecated (in ISO-8601 format) |
| `description` | `string` | Required | Description of the Image |
| `diskSize` | `number` | Required | Size of the disk contained in the Image in GB |
| `id` | `number` | Required | ID of the Resource |
| `imageSize` | `number \| null` | Required | Size of the Image file in our storage in GB. For snapshot Images this is the value relevant for calculating costs for the Image. |
| `labels` | `Record<string, string>` | Required | User-defined labels (key-value pairs) |
| `name` | `string \| null` | Required | Unique identifier of the Image. This value is only set for system Images. |
| `osFlavor` | [`OsFlavorEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/enumerations/os-flavor.md) | Required | Flavor of operating system contained in the Image |
| `osVersion` | `string \| null` | Required | Operating system version |
| `protection` | [`Protection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/protection.md) | Required | Protection configuration for the Resource |
| `rapidDeploy` | `boolean \| undefined` | Optional | Indicates that rapid deploy of the Image is available |
| `status` | [`Status24Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/enumerations/status-24.md) | Required | Whether the Image can be used or if it's still being created or unavailable |
| `type` | [`Type22Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/enumerations/type-22.md) | Required | Type of the Image |


# Example

```ts
import {
  Image,
  OsFlavorEnum,
  Status24Enum,
  Type22Enum,
} from 'hetzner-cloud-apilib';

const image: Image = {
  boundTo: null,
  created: '2016-01-30T23:55:00+00:00',
  createdFrom: {
    id: 1,
    name: 'Server',
  },
  deleted: null,
  deprecated: '2018-02-28T00:00:00+00:00',
  description: 'Ubuntu 20.04 Standard 64 bit',
  diskSize: 10,
  id: 42,
  imageSize: 2.3,
  labels: {
    'key0': 'labels4'
  },
  name: 'ubuntu-20.04',
  osFlavor: OsFlavorEnum.Ubuntu,
  osVersion: '20.04',
  protection: {
    mDelete: false,
  },
  status: Status24Enum.Unavailable,
  type: Type22Enum.Snapshot,
  rapidDeploy: false,
};
```



