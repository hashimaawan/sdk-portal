# V2 Vpcs Request 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBWcGNzJTI1MjBSZXF1ZXN0MQ

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2VpcsRequest1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `description` | `string \| undefined` | Optional | A free-form text field for describing the VPC's purpose. It may be a maximum of 255 characters.<br><br>**Constraints**: *Maximum Length*: `255` |
| `name` | `string \| undefined` | Optional | The name of the VPC. Must be unique and may only contain alphanumeric characters, dashes, and periods.<br><br>**Constraints**: *Pattern*: `^[a-zA-Z0-9\-\.]+$` |
| `mDefault` | `boolean \| undefined` | Optional | A boolean value indicating whether or not the VPC is the default network for the region. All applicable resources are placed into the default VPC network unless otherwise specified during their creation. The `default` field cannot be unset from `true`. If you want to set a new default VPC network, update the `default` field of another VPC network in the same region. The previous network's `default` field will be set to `false` when a new default VPC has been defined. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { V2VpcsRequest1 } from 'digitalocean-apilib';

const v2VpcsRequest1: V2VpcsRequest1 = {
  description: 'VPC for production environment',
  name: 'env.prod-vpc',
  mDefault: true,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



