# V2 Databases Pools Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMFBvb2xzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2DatabasesPoolsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `pools` | [`Pool[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/pool.md) | Optional, Read-only | An array of connection pool objects. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { V2DatabasesPoolsResponse } from 'digitalocean-apilib';

const v2DatabasesPoolsResponse: V2DatabasesPoolsResponse = {
  pools: [
    {
      db: 'db2',
      mode: 'mode0',
      name: 'name2',
      size: 68,
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
      user: 'user2',
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



