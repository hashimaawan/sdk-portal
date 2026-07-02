# Database

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkRhdGFiYXNl

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Database`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clusterName` | `string \| undefined` | Optional | The name of the underlying DigitalOcean DBaaS cluster. This is required for production databases. For dev databases, if cluster_name is not set, a new cluster will be provisioned. |
| `dbName` | `string \| undefined` | Optional | The name of the MySQL or PostgreSQL database to configure. |
| `dbUser` | `string \| undefined` | Optional | The name of the MySQL or PostgreSQL user to configure. |
| `engine` | [`Engine \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/engine.md) | Optional | - MYSQL: MySQL<br>- PG: PostgreSQL<br>- REDIS: Redis<br><br>**Default**: `Engine.Unset` |
| `name` | `string` | Required | The name. Must be unique across all components within the same app.<br><br>**Constraints**: *Minimum Length*: `2`, *Maximum Length*: `32`, *Pattern*: `^[a-z][a-z0-9-]{0,30}[a-z0-9]$` |
| `production` | `boolean \| undefined` | Optional | Whether this is a production or dev database. |
| `version` | `string \| undefined` | Optional | The version of the database engine |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Database, Engine } from 'digitalocean-apilib';

const database: Database = {
  name: 'prod-db',
  clusterName: 'cluster_name',
  dbName: 'my_db',
  dbUser: 'superuser',
  engine: Engine.Pg,
  production: true,
  version: '12',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



