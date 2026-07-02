# Pgbouncer

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlBnYm91bmNlcg

PGBouncer connection pooling settings

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Pgbouncer`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AutodbIdleTimeout` | `*int` | Optional | If the automatically-created database pools have been unused this many seconds, they are freed. If 0, timeout is disabled.<br><br>**Constraints**: `>= 0`, `<= 86400` |
| `AutodbMaxDbConnections` | `*int` | Optional | Only allows a maximum this many server connections per database (regardless of user). If 0, allows unlimited connections.<br><br>**Constraints**: `>= 0`, `<= 2147483647` |
| `AutodbPoolMode` | [`*models.AutodbPoolMode`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/autodb-pool-mode.md) | Optional | PGBouncer pool mode |
| `AutodbPoolSize` | `*int` | Optional | If non-zero, automatically creates a pool of that size per user when a pool doesn't exist.<br><br>**Constraints**: `>= 0`, `<= 10000` |
| `IgnoreStartupParameters` | [`[]models.IgnoreStartupParameter`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/ignore-startup-parameter.md) | Optional | List of parameters to ignore when given in startup packet.<br><br>**Constraints**: *Maximum Items*: `32` |
| `MinPoolSize` | `*int` | Optional | If current server connections are below this number, adds more. Improves behavior when usual load comes suddenly back after period of total inactivity. The value is effectively capped at the pool size.<br><br>**Constraints**: `>= 0`, `<= 10000` |
| `ServerIdleTimeout` | `*int` | Optional | Drops server connections if they have been idle more than this many seconds.  If 0, timeout is disabled.<br><br>**Constraints**: `>= 0`, `<= 86400` |
| `ServerLifetime` | `*int` | Optional | The pooler closes any unused server connection that has been connected longer than this amount of seconds.<br><br>**Constraints**: `>= 60`, `<= 86400` |
| `ServerResetQueryAlways` | `*bool` | Optional | Run server_reset_query (DISCARD ALL) in all pooling modes. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    pgbouncer := models.Pgbouncer{
        AutodbIdleTimeout:       models.ToPointer(3600),
        AutodbMaxDbConnections:  models.ToPointer(1),
        AutodbPoolMode:          models.ToPointer(models.AutodbPoolMode_Session),
        AutodbPoolSize:          models.ToPointer(1),
        IgnoreStartupParameters: []models.IgnoreStartupParameter{
            models.IgnoreStartupParameter_ExtraFloatDigits,
            models.IgnoreStartupParameter_SearchPath,
        },
        MinPoolSize:             models.ToPointer(1),
        ServerIdleTimeout:       models.ToPointer(600),
        ServerLifetime:          models.ToPointer(3600),
        ServerResetQueryAlways:  models.ToPointer(false),
        AdditionalProperties:    map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



