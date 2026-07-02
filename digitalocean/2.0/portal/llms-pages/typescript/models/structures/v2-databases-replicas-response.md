# V2 Databases Replicas Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMFJlcGxpY2FzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2DatabasesReplicasResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `replicas` | [`Replica[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/replica.md) | Optional | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { V2DatabasesReplicasResponse } from 'digitalocean-apilib';

const v2DatabasesReplicasResponse: V2DatabasesReplicasResponse = {
  replicas: [
    {
      name: 'name6',
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
      createdAt: '2016-03-13T12:52:32.123Z',
      id: '000022b6-0000-0000-0000-000000000000',
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
      privateNetworkUuid: 'private_network_uuid6',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      name: 'name6',
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
      createdAt: '2016-03-13T12:52:32.123Z',
      id: '000022b6-0000-0000-0000-000000000000',
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
      privateNetworkUuid: 'private_network_uuid6',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



