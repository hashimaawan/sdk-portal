# Pgbouncer

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlBnYm91bmNlcg

PGBouncer connection pooling settings

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`Pgbouncer`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AutodbIdleTimeout` | `int?` | Optional | If the automatically-created database pools have been unused this many seconds, they are freed. If 0, timeout is disabled.<br><br>**Constraints**: `>= 0`, `<= 86400` |
| `AutodbMaxDbConnections` | `int?` | Optional | Only allows a maximum this many server connections per database (regardless of user). If 0, allows unlimited connections.<br><br>**Constraints**: `>= 0`, `<= 2147483647` |
| `AutodbPoolMode` | [`AutodbPoolMode?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/autodb-pool-mode.md) | Optional | PGBouncer pool mode |
| `AutodbPoolSize` | `int?` | Optional | If non-zero, automatically creates a pool of that size per user when a pool doesn't exist.<br><br>**Constraints**: `>= 0`, `<= 10000` |
| `IgnoreStartupParameters` | [`List<IgnoreStartupParameter>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/ignore-startup-parameter.md) | Optional | List of parameters to ignore when given in startup packet.<br><br>**Constraints**: *Maximum Items*: `32` |
| `MinPoolSize` | `int?` | Optional | If current server connections are below this number, adds more. Improves behavior when usual load comes suddenly back after period of total inactivity. The value is effectively capped at the pool size.<br><br>**Constraints**: `>= 0`, `<= 10000` |
| `ServerIdleTimeout` | `int?` | Optional | Drops server connections if they have been idle more than this many seconds.  If 0, timeout is disabled.<br><br>**Constraints**: `>= 0`, `<= 86400` |
| `ServerLifetime` | `int?` | Optional | The pooler closes any unused server connection that has been connected longer than this amount of seconds.<br><br>**Constraints**: `>= 60`, `<= 86400` |
| `ServerResetQueryAlways` | `bool?` | Optional | Run server_reset_query (DISCARD ALL) in all pooling modes. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;

Pgbouncer pgbouncer = new Pgbouncer
{
    AutodbIdleTimeout = 3600,
    AutodbMaxDbConnections = 1,
    AutodbPoolMode = AutodbPoolMode.Session,
    AutodbPoolSize = 1,
    IgnoreStartupParameters = new List<IgnoreStartupParameter>
    {
        IgnoreStartupParameter.ExtraFloatDigits,
        IgnoreStartupParameter.SearchPath,
    },
    MinPoolSize = 1,
    ServerIdleTimeout = 600,
    ServerLifetime = 3600,
    ServerResetQueryAlways = false,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



