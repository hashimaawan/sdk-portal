# V2 Volumes Actions Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBWb2x1bWVzJTI1MjBBY3Rpb25zJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2VolumesActionsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `region` | [`Region2 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/region-2.md) | Optional | The slug identifier for the region where the resource will initially be  available. |
| `type` | [`Type21`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/type-21.md) | Required | The volume action to initiate. |
| `dropletId` | `number` | Required | The unique identifier for the Droplet the volume will be attached or detached from. |
| `tags` | `string[] \| null \| undefined` | Optional | A flat array of tag names as strings to be applied to the resource. Tag names may be for either existing or new tags. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import {
  Region2,
  Type21,
  V2VolumesActionsRequest,
} from 'digitalocean-apilib';

const v2VolumesActionsRequest: V2VolumesActionsRequest = {
  type: Type21.Attach,
  dropletId: 11612190,
  region: Region2.Nyc3,
  tags: [
    'base-image',
    'prod'
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



