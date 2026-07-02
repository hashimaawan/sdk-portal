# Database 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkRhdGFiYXNlMQ

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Database1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `connection` | [`Connection \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/connection.md) | Optional | - |
| `createdAt` | `string \| undefined` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the database cluster was created. |
| `dbNames` | `string[] \| null \| undefined` | Optional, Read-only | An array of strings containing the names of databases created in the database cluster. |
| `engine` | [`Engine1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/engine-1.md) | Required | A slug representing the database engine used for the cluster. The possible values are: "pg" for PostgreSQL, "mysql" for MySQL, "redis" for Redis, and "mongodb" for MongoDB. |
| `id` | `string \| undefined` | Optional, Read-only | A unique ID that can be used to identify and reference a database cluster. |
| `maintenanceWindow` | [`MaintenanceWindow \| null \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/maintenance-window.md) | Optional | - |
| `name` | `string` | Required | A unique, human-readable name referring to a database cluster. |
| `numNodes` | `number` | Required | The number of nodes in the database cluster. |
| `privateConnection` | [`PrivateConnection \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/private-connection.md) | Optional | - |
| `privateNetworkUuid` | `string \| undefined` | Optional | A string specifying the UUID of the VPC to which the database cluster will be assigned. If excluded, the cluster when creating a new database cluster, it will be assigned to your account's default VPC for the region.<br><br>**Constraints**: *Pattern*: `^$\|[0-9a-f]{8}\b-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{4}-\b[0-9a-f]{12}` |
| `projectId` | `string \| undefined` | Optional | The ID of the project that the database cluster is assigned to. If excluded when creating a new database cluster, it will be assigned to your default project. |
| `region` | `string` | Required | The slug identifier for the region where the database cluster is located. |
| `rules` | [`Rule1[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/rule-1.md) | Optional | - |
| `size` | `string` | Required | The slug identifier representing the size of the nodes in the database cluster. |
| `status` | [`Status4 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/status-4.md) | Optional, Read-only | A string representing the current status of the database cluster. |
| `tags` | `string[] \| null \| undefined` | Optional | An array of tags that have been applied to the database cluster. |
| `users` | [`User[] \| null \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/user.md) | Optional, Read-only | - |
| `version` | `string \| undefined` | Optional | A string representing the version of the database engine in use for the cluster. |
| `versionEndOfAvailability` | `string \| undefined` | Optional, Read-only | A timestamp referring to the date when the particular version will no longer be available for creating new clusters. If null, the version does not have an end of availability timeline. |
| `versionEndOfLife` | `string \| undefined` | Optional, Read-only | A timestamp referring to the date when the particular version will no longer be supported. If null, the version does not have an end of life timeline. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Database1, Engine1, Status4 } from 'digitalocean-apilib';

const database1: Database1 = {
  engine: Engine1.Pg,
  name: 'backend',
  numNodes: 2,
  region: 'nyc3',
  size: 'db-s-2vcpu-4gb',
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
  dbNames: [
    'doadmin'
  ],
  id: '9cc10173-e9ea-4176-9dbc-a4cee4c4ff30',
  maintenanceWindow: {
    day: 'day0',
    hour: 'hour8',
    description: [
      'description3',
      'description2'
    ],
    pending: false,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  privateNetworkUuid: 'd455e75d-4858-4eec-8c95-da2f0a5f93a7',
  projectId: '9cc10173-e9ea-4176-9dbc-a4cee4c4ff30',
  status: Status4.Creating,
  tags: [
    'production'
  ],
  version: '10',
  versionEndOfAvailability: '2023-05-09T00:00:00Z',
  versionEndOfLife: '2023-11-09T00:00:00Z',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



