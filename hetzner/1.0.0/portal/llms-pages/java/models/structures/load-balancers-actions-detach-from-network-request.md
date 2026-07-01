# Load Balancers Actions Detach from Network Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwQWN0aW9ucyUyNTIwRGV0YWNoJTI1MjBGcm9tJTI1MjBOZXR3b3JrJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type Object.*


# Class Name

`LoadBalancersActionsDetachFromNetworkRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Network` | `double` | Required | ID of an existing network to detach the Load Balancer from | double getNetwork() | setNetwork(double network) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.LoadBalancersActionsDetachFromNetworkRequest;
import java.io.IOException;

LoadBalancersActionsDetachFromNetworkRequest loadBalancersActionsDetachFromNetworkRequest = new LoadBalancersActionsDetachFromNetworkRequest.Builder(
    4711D
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



