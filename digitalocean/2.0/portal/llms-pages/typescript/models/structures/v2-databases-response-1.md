# V2 Databases Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMFJlc3BvbnNlMQ

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2DatabasesResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `database` | [`Database1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/database-1.md) | Required | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Engine1, Status4, V2DatabasesResponse1 } from 'digitalocean-apilib';

const v2DatabasesResponse1: V2DatabasesResponse1 = {
  database: {
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
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



