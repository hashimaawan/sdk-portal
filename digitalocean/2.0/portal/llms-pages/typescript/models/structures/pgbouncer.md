# Pgbouncer

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlBnYm91bmNlcg

PGBouncer connection pooling settings

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Pgbouncer`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `autodbIdleTimeout` | `number \| undefined` | Optional | If the automatically-created database pools have been unused this many seconds, they are freed. If 0, timeout is disabled.<br><br>**Constraints**: `>= 0`, `<= 86400` |
| `autodbMaxDbConnections` | `number \| undefined` | Optional | Only allows a maximum this many server connections per database (regardless of user). If 0, allows unlimited connections.<br><br>**Constraints**: `>= 0`, `<= 2147483647` |
| `autodbPoolMode` | [`AutodbPoolMode \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/autodb-pool-mode.md) | Optional | PGBouncer pool mode |
| `autodbPoolSize` | `number \| undefined` | Optional | If non-zero, automatically creates a pool of that size per user when a pool doesn't exist.<br><br>**Constraints**: `>= 0`, `<= 10000` |
| `ignoreStartupParameters` | [`IgnoreStartupParameter[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/ignore-startup-parameter.md) | Optional | List of parameters to ignore when given in startup packet.<br><br>**Constraints**: *Maximum Items*: `32` |
| `minPoolSize` | `number \| undefined` | Optional | If current server connections are below this number, adds more. Improves behavior when usual load comes suddenly back after period of total inactivity. The value is effectively capped at the pool size.<br><br>**Constraints**: `>= 0`, `<= 10000` |
| `serverIdleTimeout` | `number \| undefined` | Optional | Drops server connections if they have been idle more than this many seconds.  If 0, timeout is disabled.<br><br>**Constraints**: `>= 0`, `<= 86400` |
| `serverLifetime` | `number \| undefined` | Optional | The pooler closes any unused server connection that has been connected longer than this amount of seconds.<br><br>**Constraints**: `>= 60`, `<= 86400` |
| `serverResetQueryAlways` | `boolean \| undefined` | Optional | Run server_reset_query (DISCARD ALL) in all pooling modes. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import {
  AutodbPoolMode,
  IgnoreStartupParameter,
  Pgbouncer,
} from 'digitalocean-apilib';

const pgbouncer: Pgbouncer = {
  autodbIdleTimeout: 3600,
  autodbMaxDbConnections: 1,
  autodbPoolMode: AutodbPoolMode.Session,
  autodbPoolSize: 1,
  ignoreStartupParameters: [
    IgnoreStartupParameter.ExtraFloatDigits,
    IgnoreStartupParameter.SearchPath
  ],
  minPoolSize: 1,
  serverIdleTimeout: 600,
  serverLifetime: 3600,
  serverResetQueryAlways: false,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



