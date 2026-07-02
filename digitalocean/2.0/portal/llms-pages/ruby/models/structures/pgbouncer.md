# Pgbouncer

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlBnYm91bmNlcg

PGBouncer connection pooling settings

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`Pgbouncer`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `autodb_idle_timeout` | `Integer` | Optional | If the automatically-created database pools have been unused this many seconds, they are freed. If 0, timeout is disabled.<br><br>**Constraints**: `>= 0`, `<= 86400` |
| `autodb_max_db_connections` | `Integer` | Optional | Only allows a maximum this many server connections per database (regardless of user). If 0, allows unlimited connections.<br><br>**Constraints**: `>= 0`, `<= 2147483647` |
| `autodb_pool_mode` | [`AutodbPoolMode`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/autodb-pool-mode.md) | Optional | PGBouncer pool mode |
| `autodb_pool_size` | `Integer` | Optional | If non-zero, automatically creates a pool of that size per user when a pool doesn't exist.<br><br>**Constraints**: `>= 0`, `<= 10000` |
| `ignore_startup_parameters` | [`Array[IgnoreStartupParameter]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/ignore-startup-parameter.md) | Optional | List of parameters to ignore when given in startup packet.<br><br>**Constraints**: *Maximum Items*: `32` |
| `min_pool_size` | `Integer` | Optional | If current server connections are below this number, adds more. Improves behavior when usual load comes suddenly back after period of total inactivity. The value is effectively capped at the pool size.<br><br>**Constraints**: `>= 0`, `<= 10000` |
| `server_idle_timeout` | `Integer` | Optional | Drops server connections if they have been idle more than this many seconds.  If 0, timeout is disabled.<br><br>**Constraints**: `>= 0`, `<= 86400` |
| `server_lifetime` | `Integer` | Optional | The pooler closes any unused server connection that has been connected longer than this amount of seconds.<br><br>**Constraints**: `>= 60`, `<= 86400` |
| `server_reset_query_always` | `TrueClass \| FalseClass` | Optional | Run server_reset_query (DISCARD ALL) in all pooling modes. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
pgbouncer = Pgbouncer.new(
  autodb_idle_timeout: 3600,
  autodb_max_db_connections: 1,
  autodb_pool_mode: AutodbPoolMode::SESSION,
  autodb_pool_size: 1,
  ignore_startup_parameters: [
    IgnoreStartupParameter::EXTRA_FLOAT_DIGITS,
    IgnoreStartupParameter::SEARCH_PATH
  ],
  min_pool_size: 1,
  server_idle_timeout: 600,
  server_lifetime: 3600,
  server_reset_query_always: false,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



