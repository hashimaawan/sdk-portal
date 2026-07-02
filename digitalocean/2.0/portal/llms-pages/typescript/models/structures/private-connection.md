# Private Connection

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlByaXZhdGVDb25uZWN0aW9u

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`PrivateConnection`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `database` | `string \| undefined` | Optional, Read-only | The name of the default database. |
| `host` | `string \| undefined` | Optional, Read-only | The FQDN pointing to the database cluster's current primary node. |
| `password` | `string \| undefined` | Optional, Read-only | The randomly generated password for the default user. |
| `port` | `number \| undefined` | Optional, Read-only | The port on which the database cluster is listening. |
| `ssl` | `boolean \| undefined` | Optional, Read-only | A boolean value indicating if the connection should be made over SSL. |
| `uri` | `string \| undefined` | Optional, Read-only | A connection string in the format accepted by the `psql` command. This is provided as a convenience and should be able to be constructed by the other attributes. |
| `user` | `string \| undefined` | Optional, Read-only | The default user for the database. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { PrivateConnection } from 'digitalocean-apilib';

const privateConnection: PrivateConnection = {
  database: 'defaultdb',
  host: 'backend-do-user-19081923-0.db.ondigitalocean.com',
  password: 'wv78n3zpz42xezdk',
  port: 25060,
  ssl: true,
  uri: 'postgres://doadmin:wv78n3zpz42xezdk@backend-do-user-19081923-0.db.ondigitalocean.com:25060/defaultdb?sslmode=require',
  user: 'doadmin',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



