# Health Check 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkhlYWx0aENoZWNrMQ

An object specifying health check settings for the load balancer.

*This model accepts additional fields of type Object.*


# Class Name

`HealthCheck1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CheckIntervalSeconds` | `Integer` | Optional | The number of seconds between between two consecutive health checks.<br><br>**Default**: `10` | Integer getCheckIntervalSeconds() | setCheckIntervalSeconds(Integer checkIntervalSeconds) |
| `HealthyThreshold` | `Integer` | Optional | The number of times a health check must pass for a backend Droplet to be marked "healthy" and be re-added to the pool.<br><br>**Default**: `3` | Integer getHealthyThreshold() | setHealthyThreshold(Integer healthyThreshold) |
| `Path` | `String` | Optional | The path on the backend Droplets to which the load balancer instance will send a request.<br><br>**Default**: `"/"` | String getPath() | setPath(String path) |
| `Port` | `Integer` | Optional | An integer representing the port on the backend Droplets on which the health check will attempt a connection.<br><br>**Default**: `80` | Integer getPort() | setPort(Integer port) |
| `Protocol` | [`Protocol1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/protocol-1.md) | Optional | The protocol used for health checks sent to the backend Droplets. The possible values are `http`, `https`, or `tcp`.<br><br>**Default**: `Protocol1.HTTP` | Protocol1 getProtocol() | setProtocol(Protocol1 protocol) |
| `ResponseTimeoutSeconds` | `Integer` | Optional | The number of seconds the load balancer instance will wait for a response until marking a health check as failed.<br><br>**Default**: `5` | Integer getResponseTimeoutSeconds() | setResponseTimeoutSeconds(Integer responseTimeoutSeconds) |
| `UnhealthyThreshold` | `Integer` | Optional | The number of times a health check must fail for a backend Droplet to be marked "unhealthy" and be removed from the pool.<br><br>**Default**: `5` | Integer getUnhealthyThreshold() | setUnhealthyThreshold(Integer unhealthyThreshold) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.HealthCheck1;
import com.digitalocean.api.models.Protocol1;
import java.io.IOException;

HealthCheck1 healthCheck1 = new HealthCheck1.Builder()
    .checkIntervalSeconds(10)
    .healthyThreshold(3)
    .path("/")
    .port(80)
    .protocol(Protocol1.HTTP)
    .responseTimeoutSeconds(5)
    .unhealthyThreshold(5)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



