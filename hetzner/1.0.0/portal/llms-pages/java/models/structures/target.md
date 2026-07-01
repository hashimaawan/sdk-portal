# Target

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlRhcmdldA

*This model accepts additional fields of type Object.*


# Class Name

`Target`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `HealthStatus` | [`List<HealthStatus>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/health-status.md) | Optional | - | List<HealthStatus> getHealthStatus() | setHealthStatus(List<HealthStatus> healthStatus) |
| `Server` | [`Server11`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/server-11.md) | Optional | - | Server11 getServer() | setServer(Server11 server) |
| `Type` | `String` | Optional | - | String getType() | setType(String type) |
| `UsePrivateIp` | `Boolean` | Optional | - | Boolean getUsePrivateIp() | setUsePrivateIp(Boolean usePrivateIp) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.HealthStatus;
import cloud.hetzner.api.models.Server11;
import cloud.hetzner.api.models.Status30;
import cloud.hetzner.api.models.Target;
import java.io.IOException;
import java.util.Arrays;

Target target = new Target.Builder()
    .healthStatus(Arrays.asList(
        new HealthStatus.Builder()
            .listenPort(142)
            .status(Status30.UNKNOWN)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new HealthStatus.Builder()
            .listenPort(142)
            .status(Status30.UNKNOWN)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new HealthStatus.Builder()
            .listenPort(142)
            .status(Status30.UNKNOWN)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
    .server(new Server11.Builder(
        14
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build())
    .type("server")
    .usePrivateIp(false)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



