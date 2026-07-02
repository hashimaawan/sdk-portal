# Replica

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlJlcGxpY2E

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Replica`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `connection` | [`Connection \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/connection.md) | Optional | - |
| `createdAt` | `string \| undefined` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the database cluster was created. |
| `id` | `string \| undefined` | Optional, Read-only | A unique ID that can be used to identify and reference a database replica. |
| `name` | `string` | Required | The name to give the read-only replicating |
| `privateConnection` | [`PrivateConnection \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/private-connection.md) | Optional | - |
| `privateNetworkUuid` | `string \| undefined` | Optional | A string specifying the UUID of the VPC to which the read-only replica will be assigned. If excluded, the replica will be assigned to your account's default VPC for the region. |
| `region` | `string \| undefined` | Optional | A slug identifier for the region where the read-only replica will be located. If excluded, the replica will be placed in the same region as the cluster. |
| `size` | `string \| undefined` | Optional | A slug identifier representing the size of the node for the read-only replica. The size of the replica must be at least as large as the node size for the database cluster from which it is replicating. |
| `status` | [`Status4 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/status-4.md) | Optional, Read-only | A string representing the current status of the database cluster. |
| `tags` | `string[] \| undefined` | Optional | A flat array of tag names as strings to apply to the read-only replica after it is created. Tag names can either be existing or new tags. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Replica, Status4 } from 'digitalocean-apilib';

const replica: Replica = {
  name: 'read-nyc3-01',
  connection: {
    database: 'database2',
    host: 'host0',
    password: 'password2',
    port: 174,
    ssl: false,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  createdAt: '2019-01-11T18:37:36Z',
  id: '9cc10173-e9ea-4176-9dbc-a4cee4c4ff30',
  privateConnection: {
    database: 'database4',
    host: 'host4',
    password: 'password8',
    port: 228,
    ssl: false,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  privateNetworkUuid: '9423cbad-9211-442f-820b-ef6915e99b5f',
  region: 'nyc3',
  size: 'db-s-2vcpu-4gb',
  status: Status4.Creating,
  tags: [
    'production'
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



