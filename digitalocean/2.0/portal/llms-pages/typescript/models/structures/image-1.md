# Image 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkltYWdlMQ

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Image1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `createdAt` | `string \| undefined` | Optional | A time value given in ISO8601 combined date and time format that represents when the image was created. |
| `description` | `string \| undefined` | Optional | An optional free-form text field to describe an image. |
| `distribution` | [`Distribution \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/distribution.md) | Optional | The name of a custom image's distribution. Currently, the valid values are  `Arch Linux`, `CentOS`, `CoreOS`, `Debian`, `Fedora`, `Fedora Atomic`,  `FreeBSD`, `Gentoo`, `openSUSE`, `RancherOS`, `Rocky Linux`, `Ubuntu`, and `Unknown`.  Any other value will be accepted but ignored, and `Unknown` will be used in its place. |
| `errorMessage` | `string \| undefined` | Optional | A string containing information about errors that may occur when importing<br>a custom image. |
| `id` | `number \| undefined` | Optional, Read-only | A unique number that can be used to identify and reference a specific image. |
| `minDiskSize` | `number \| null \| undefined` | Optional | The minimum disk size in GB required for a Droplet to use this image.<br><br>**Constraints**: `>= 0` |
| `name` | `string \| undefined` | Optional | The display name that has been given to an image.  This is what is shown in the control panel and is generally a descriptive title for the image in question. |
| `mPublic` | `boolean \| undefined` | Optional | This is a boolean value that indicates whether the image in question is public or not. An image that is public is available to all accounts. A non-public image is only accessible from your account. |
| `regions` | [`Region2[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/region-2.md) | Optional | This attribute is an array of the regions that the image is available in. The regions are represented by their identifying slug values. |
| `sizeGigabytes` | `number \| null \| undefined` | Optional | The size of the image in gigabytes. |
| `slug` | `string \| null \| undefined` | Optional | A uniquely identifying string that is associated with each of the DigitalOcean-provided public images. These can be used to reference a public image as an alternative to the numeric id. |
| `status` | [`Status7 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/status-7.md) | Optional | A status string indicating the state of a custom image. This may be `NEW`,<br>`available`, `pending`, `deleted`, or `retired`. |
| `tags` | `string[] \| null \| undefined` | Optional | A flat array of tag names as strings to be applied to the resource. Tag names may be for either existing or new tags. |
| `type` | [`Type9 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/type-9.md) | Optional | Describes the kind of image. It may be one of `base`, `snapshot`, `backup`, `custom`, or `admin`. Respectively, this specifies whether an image is a DigitalOcean base OS image, user-generated Droplet snapshot, automatically created Droplet backup, user-provided virtual machine image, or an image used for DigitalOcean managed resources (e.g. DOKS worker nodes). |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import {
  Distribution,
  Image1,
  Region2,
  Status7,
  Type9,
} from 'digitalocean-apilib';

const image1: Image1 = {
  createdAt: '2020-05-04T22:23:02Z',
  description: 'description2',
  distribution: Distribution.Ubuntu,
  errorMessage: 'error_message0',
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
};
```



