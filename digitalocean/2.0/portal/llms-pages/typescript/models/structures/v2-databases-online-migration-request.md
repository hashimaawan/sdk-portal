# V2 Databases Online Migration Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyME9ubGluZSUyNTIwTWlncmF0aW9uJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2DatabasesOnlineMigrationRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `disableSsl` | `boolean \| undefined` | Optional | Enables SSL encryption when connecting to the source database. |
| `source` | [`Source \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/source.md) | Optional | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { V2DatabasesOnlineMigrationRequest } from 'digitalocean-apilib';

const v2DatabasesOnlineMigrationRequest: V2DatabasesOnlineMigrationRequest = {
  disableSsl: false,
  source: {
    database: 'database4',
    host: 'host4',
    password: 'password8',
    port: 180,
    ssl: false,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



