# Action 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkFjdGlvbjI

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Action2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `completedAt` | `string \| null \| undefined` | Optional | A time value given in ISO8601 combined date and time format that represents when the action was completed. |
| `id` | `number \| undefined` | Optional | A unique numeric ID that can be used to identify and reference an action. |
| `region` | [`Region \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/region.md) | Optional | - |
| `regionSlug` | `string \| null \| undefined` | Optional | - |
| `resourceId` | `number \| null \| undefined` | Optional | A unique identifier for the resource that the action is associated with. |
| `resourceType` | `string \| undefined` | Optional | The type of resource that the action is associated with. |
| `startedAt` | `string \| undefined` | Optional | A time value given in ISO8601 combined date and time format that represents when the action was initiated. |
| `status` | [`Status1 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/status-1.md) | Optional | The current status of the action. This can be "in-progress", "completed", or "errored".<br><br>**Default**: `Status1.Inprogress` |
| `type` | `string \| undefined` | Optional | This is the type of action that the object represents. For example, this could be "transfer" to represent the state of an image transfer action. |
| `projectId` | `string \| undefined` | Optional | The UUID of the project to which the reserved IP currently belongs. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Action2, Status1 } from 'digitalocean-apilib';

const action2: Action2 = {
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
  regionSlug: 'region_slug8',
  resourceId: 3164444,
  resourceType: 'droplet',
  startedAt: '2020-11-14T16:29:21Z',
  status: Status1.Completed,
  type: 'create',
  projectId: '746c6152-2fa2-11ed-92d3-27aaa54e4988',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



