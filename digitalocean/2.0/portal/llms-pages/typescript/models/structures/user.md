# User

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlVzZXI

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`User`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `mysqlSettings` | [`MysqlSettings \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/mysql-settings.md) | Optional | - |
| `name` | `string` | Required | The name of a database user. |
| `password` | `string \| undefined` | Optional, Read-only | A randomly generated password for the database user. |
| `role` | [`Role \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/role.md) | Optional, Read-only | A string representing the database user's role. The value will be either<br>"primary" or "normal". |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { AuthPlugin, Role, User } from 'digitalocean-apilib';

const user: User = {
  name: 'app-01',
  mysqlSettings: {
    authPlugin: AuthPlugin.MysqlNativePassword,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  password: 'jge5lfxtzhx42iff',
  role: Role.Normal,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



