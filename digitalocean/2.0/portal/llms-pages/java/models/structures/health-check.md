# Health Check

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkhlYWx0aENoZWNr

*This model accepts additional fields of type Object.*


# Class Name

`HealthCheck`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `FailureThreshold` | `Integer` | Optional | The number of failed health checks before considered unhealthy. | Integer getFailureThreshold() | setFailureThreshold(Integer failureThreshold) |
| `HttpPath` | `String` | Optional | The route path used for the HTTP health check ping. If not set, the HTTP health check will be disabled and a TCP health check used instead. | String getHttpPath() | setHttpPath(String httpPath) |
| `InitialDelaySeconds` | `Integer` | Optional | The number of seconds to wait before beginning health checks. | Integer getInitialDelaySeconds() | setInitialDelaySeconds(Integer initialDelaySeconds) |
| `PeriodSeconds` | `Integer` | Optional | The number of seconds to wait between health checks. | Integer getPeriodSeconds() | setPeriodSeconds(Integer periodSeconds) |
| `Port` | `Long` | Optional | The port on which the health check will be performed. If not set, the health check will be performed on the component's http_port.<br><br>**Constraints**: `>= 1`, `<= 65535` | Long getPort() | setPort(Long port) |
| `SuccessThreshold` | `Integer` | Optional | The number of successful health checks before considered healthy. | Integer getSuccessThreshold() | setSuccessThreshold(Integer successThreshold) |
| `TimeoutSeconds` | `Integer` | Optional | The number of seconds after which the check times out. | Integer getTimeoutSeconds() | setTimeoutSeconds(Integer timeoutSeconds) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.HealthCheck;
import java.io.IOException;

HealthCheck healthCheck = new HealthCheck.Builder()
    .failureThreshold(2)
    .httpPath("/health")
    .initialDelaySeconds(30)
    .periodSeconds(60)
    .port(80L)
    .successThreshold(3)
    .timeoutSeconds(45)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



