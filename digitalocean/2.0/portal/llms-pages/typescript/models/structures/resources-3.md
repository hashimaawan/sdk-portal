# Resources 3

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlJlc291cmNlczM

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Resources3`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `resourceId` | `string \| undefined` | Optional | The identifier of a resource. |
| `resourceType` | [`ResourceType2 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/resource-type-2.md) | Optional | The type of the resource. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { ResourceType2, Resources3 } from 'digitalocean-apilib';

const resources3: Resources3 = {
  resourceId: '3d80cb72-342b-4aaa-b92e-4e4abb24a933',
  resourceType: ResourceType2.Volume,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



