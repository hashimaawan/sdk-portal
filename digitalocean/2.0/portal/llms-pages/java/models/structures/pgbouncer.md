# Pgbouncer

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlBnYm91bmNlcg

PGBouncer connection pooling settings

*This model accepts additional fields of type Object.*


# Class Name

`Pgbouncer`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AutodbIdleTimeout` | `Integer` | Optional | If the automatically-created database pools have been unused this many seconds, they are freed. If 0, timeout is disabled.<br><br>**Constraints**: `>= 0`, `<= 86400` | Integer getAutodbIdleTimeout() | setAutodbIdleTimeout(Integer autodbIdleTimeout) |
| `AutodbMaxDbConnections` | `Integer` | Optional | Only allows a maximum this many server connections per database (regardless of user). If 0, allows unlimited connections.<br><br>**Constraints**: `>= 0`, `<= 2147483647` | Integer getAutodbMaxDbConnections() | setAutodbMaxDbConnections(Integer autodbMaxDbConnections) |
| `AutodbPoolMode` | [`AutodbPoolMode`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/autodb-pool-mode.md) | Optional | PGBouncer pool mode | AutodbPoolMode getAutodbPoolMode() | setAutodbPoolMode(AutodbPoolMode autodbPoolMode) |
| `AutodbPoolSize` | `Integer` | Optional | If non-zero, automatically creates a pool of that size per user when a pool doesn't exist.<br><br>**Constraints**: `>= 0`, `<= 10000` | Integer getAutodbPoolSize() | setAutodbPoolSize(Integer autodbPoolSize) |
| `IgnoreStartupParameters` | [`List<IgnoreStartupParameter>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/ignore-startup-parameter.md) | Optional | List of parameters to ignore when given in startup packet.<br><br>**Constraints**: *Maximum Items*: `32` | List<IgnoreStartupParameter> getIgnoreStartupParameters() | setIgnoreStartupParameters(List<IgnoreStartupParameter> ignoreStartupParameters) |
| `MinPoolSize` | `Integer` | Optional | If current server connections are below this number, adds more. Improves behavior when usual load comes suddenly back after period of total inactivity. The value is effectively capped at the pool size.<br><br>**Constraints**: `>= 0`, `<= 10000` | Integer getMinPoolSize() | setMinPoolSize(Integer minPoolSize) |
| `ServerIdleTimeout` | `Integer` | Optional | Drops server connections if they have been idle more than this many seconds.  If 0, timeout is disabled.<br><br>**Constraints**: `>= 0`, `<= 86400` | Integer getServerIdleTimeout() | setServerIdleTimeout(Integer serverIdleTimeout) |
| `ServerLifetime` | `Integer` | Optional | The pooler closes any unused server connection that has been connected longer than this amount of seconds.<br><br>**Constraints**: `>= 60`, `<= 86400` | Integer getServerLifetime() | setServerLifetime(Integer serverLifetime) |
| `ServerResetQueryAlways` | `Boolean` | Optional | Run server_reset_query (DISCARD ALL) in all pooling modes. | Boolean getServerResetQueryAlways() | setServerResetQueryAlways(Boolean serverResetQueryAlways) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.AutodbPoolMode;
import com.digitalocean.api.models.IgnoreStartupParameter;
import com.digitalocean.api.models.Pgbouncer;
import java.io.IOException;
import java.util.Arrays;

Pgbouncer pgbouncer = new Pgbouncer.Builder()
    .autodbIdleTimeout(3600)
    .autodbMaxDbConnections(1)
    .autodbPoolMode(AutodbPoolMode.SESSION)
    .autodbPoolSize(1)
    .ignoreStartupParameters(Arrays.asList(
        IgnoreStartupParameter.EXTRA_FLOAT_DIGITS,
        IgnoreStartupParameter.SEARCH_PATH
    ))
    .minPoolSize(1)
    .serverIdleTimeout(600)
    .serverLifetime(3600)
    .serverResetQueryAlways(false)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



