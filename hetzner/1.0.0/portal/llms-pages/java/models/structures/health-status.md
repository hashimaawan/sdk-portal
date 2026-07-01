# Health Status

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkhlYWx0aFN0YXR1cw


# Class Name

`HealthStatus`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ListenPort` | `Integer` | Optional | - | Integer getListenPort() | setListenPort(Integer listenPort) |
| `Status` | [`Status30Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/status-30.md) | Optional | - | Status30Enum getStatus() | setStatus(Status30Enum status) |


# Example

```java
import cloud.hetzner.api.models.HealthStatus;
import cloud.hetzner.api.models.Status30Enum;

HealthStatus healthStatus = new HealthStatus.Builder()
    .listenPort(443)
    .status(Status30Enum.HEALTHY)
    .build();
```



