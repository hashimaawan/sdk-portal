# Region

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlJlZ2lvbg

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Region`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `available` | `boolean` | Required | This is a boolean value that represents whether new Droplets can be created in this region. |
| `features` | `string[]` | Required | This attribute is set to an array which contains features available in this region |
| `name` | `string` | Required | The display name of the region.  This will be a full name that is used in the control panel and other interfaces. |
| `sizes` | `string[]` | Required | This attribute is set to an array which contains the identifying slugs for the sizes available in this region. |
| `slug` | `string` | Required | A human-readable string that is used as a unique identifier for each region. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Region } from 'digitalocean-apilib';

const region: Region = {
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
};
```



