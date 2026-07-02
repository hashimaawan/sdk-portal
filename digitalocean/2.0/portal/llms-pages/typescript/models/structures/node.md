# Node

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRk5vZGU

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Node`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `createdAt` | `string \| undefined` | Optional | A time value given in ISO8601 combined date and time format that represents when the node was created. |
| `dropletId` | `string \| undefined` | Optional | The ID of the Droplet used for the worker node. |
| `id` | `string \| undefined` | Optional | A unique ID that can be used to identify and reference the node. |
| `name` | `string \| undefined` | Optional | An automatically generated, human-readable name for the node. |
| `status` | [`Status10 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/status-10.md) | Optional | An object containing a `state` attribute whose value is set to a string indicating the current status of the node. |
| `updatedAt` | `string \| undefined` | Optional | A time value given in ISO8601 combined date and time format that represents when the node was last updated. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Node, State1 } from 'digitalocean-apilib';

const node: Node = {
  createdAt: '2018-11-15T16:00:11Z',
  dropletId: '205545370',
  id: 'e78247f8-b1bb-4f7a-8db9-2a5f8d4b8f8f',
  name: 'adoring-newton-3niq',
  status: {
    state: State1.Provisioning,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  updatedAt: '2018-11-15T16:00:11Z',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



