# V2 Images Actions Request 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBJbWFnZXMlMjUyMEFjdGlvbnMlMjUyMFJlcXVlc3Qx

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2ImagesActionsRequest1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | [`Type15`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/type-15.md) | Required | The action to be taken on the image. Can be either `convert` or `transfer`. |
| `region` | [`Region2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/region-2.md) | Required | The slug identifier for the region where the resource will initially be  available. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import {
  Region2,
  Type15,
  V2ImagesActionsRequest1,
} from 'digitalocean-apilib';

const v2ImagesActionsRequest1: V2ImagesActionsRequest1 = {
  type: Type15.Convert,
  region: Region2.Nyc3,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



