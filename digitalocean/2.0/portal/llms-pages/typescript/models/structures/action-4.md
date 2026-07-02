# Action 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkFjdGlvbjQ

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Action4`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `resourceId` | `number \| null \| undefined` | Optional | A unique identifier for the resource that the action is associated with. |
| `type` | `string \| undefined` | Optional | This is the type of action that the object represents. For example, this could be "attach_volume" to represent the state of a volume attach action. |
| `completedAt` | `string \| null \| undefined` | Optional | A time value given in ISO8601 combined date and time format that represents when the action was completed. |
| `id` | `number \| undefined` | Optional | A unique numeric ID that can be used to identify and reference an action. |
| `region` | [`Region \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/region.md) | Optional | - |
| `regionSlug` | `string \| null \| undefined` | Optional | - |
| `resourceType` | `string \| undefined` | Optional | The type of resource that the action is associated with. |
| `startedAt` | `string \| undefined` | Optional | A time value given in ISO8601 combined date and time format that represents when the action was initiated. |
| `status` | [`Status1 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/status-1.md) | Optional | The current status of the action. This can be "in-progress", "completed", or "errored".<br><br>**Default**: `Status1.Inprogress` |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Action4, Status1 } from 'digitalocean-apilib';

const action4: Action4 = {
  resourceId: 160,
  type: 'attach_volume',
  completedAt: '2020-11-14T16:30:06Z',
  id: 36804636,
  region: {
    available: false,
    features: [
      'features7',
      'features8',
      'features9'
    ],
    name: 'name6',
    sizes: [
      'sizes6'
    ],
    slug: 'slug0',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  resourceType: 'droplet',
  startedAt: '2020-11-14T16:29:21Z',
  status: Status1.Completed,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



