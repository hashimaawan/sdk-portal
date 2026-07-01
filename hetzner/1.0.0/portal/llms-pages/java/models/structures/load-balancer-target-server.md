# Load Balancer Target Server

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclRhcmdldFNlcnZlcg

Server where the traffic should be routed through

*This model accepts additional fields of type Object.*


# Class Name

`LoadBalancerTargetServer`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `int` | Required | ID of the Server | int getId() | setId(int id) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.LoadBalancerTargetServer;
import java.io.IOException;

LoadBalancerTargetServer loadBalancerTargetServer = new LoadBalancerTargetServer.Builder(
    80
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



