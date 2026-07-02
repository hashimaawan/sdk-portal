# V2 Databases Pools Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMFBvb2xzJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2DatabasesPoolsResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `pool` | [`Pool`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/pool.md) | Required | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { V2DatabasesPoolsResponse1 } from 'digitalocean-apilib';

const v2DatabasesPoolsResponse1: V2DatabasesPoolsResponse1 = {
  pool: {
    db: 'defaultdb',
    mode: 'transaction',
    name: 'backend-pool',
    size: 10,
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
    user: 'doadmin',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



