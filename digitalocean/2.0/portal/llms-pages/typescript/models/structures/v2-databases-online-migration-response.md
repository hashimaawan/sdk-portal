# V2 Databases Online Migration Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyME9ubGluZSUyNTIwTWlncmF0aW9uJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2DatabasesOnlineMigrationResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `createdAt` | `string \| undefined` | Optional | The time the migration was initiated, in ISO 8601 format. |
| `id` | `string \| undefined` | Optional | The ID of the most recent migration. |
| `status` | [`Status5 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/status-5.md) | Optional | The current status of the migration. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import {
  Status5,
  V2DatabasesOnlineMigrationResponse,
} from 'digitalocean-apilib';

const v2DatabasesOnlineMigrationResponse: V2DatabasesOnlineMigrationResponse = {
  createdAt: '2020-10-29T15:57:38Z',
  id: '77b28fc8-19ff-11eb-8c9c-c68e24557488',
  status: Status5.Running,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



