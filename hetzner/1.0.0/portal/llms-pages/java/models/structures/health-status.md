# Health Status

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkhlYWx0aFN0YXR1cw

*This model accepts additional fields of type Object.*


# Class Name

`HealthStatus`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ListenPort` | `Integer` | Optional | - | Integer getListenPort() | setListenPort(Integer listenPort) |
| `Status` | [`Status30`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/status-30.md) | Optional | - | Status30 getStatus() | setStatus(Status30 status) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.HealthStatus;
import cloud.hetzner.api.models.Status30;
import java.io.IOException;

HealthStatus healthStatus = new HealthStatus.Builder()
    .listenPort(443)
    .status(Status30.HEALTHY)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



