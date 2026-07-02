# Mysql Settings

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRk15c3FsU2V0dGluZ3M

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`MysqlSettings`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `authPlugin` | [`AuthPlugin`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/auth-plugin.md) | Required | A string specifying the authentication method to be used for connections<br>to the MySQL user account. The valid values are `mysql_native_password`<br>or `caching_sha2_password`. If excluded when creating a new user, the<br>default for the version of MySQL in use will be used. As of MySQL 8.0, the<br>default is `caching_sha2_password`. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { AuthPlugin, MysqlSettings } from 'digitalocean-apilib';

const mysqlSettings: MysqlSettings = {
  authPlugin: AuthPlugin.MysqlNativePassword,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



