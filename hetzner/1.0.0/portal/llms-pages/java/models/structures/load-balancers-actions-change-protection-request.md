# Load Balancers Actions Change Protection Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwQWN0aW9ucyUyNTIwQ2hhbmdlJTI1MjBQcm90ZWN0aW9uJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type Object.*


# Class Name

`LoadBalancersActionsChangeProtectionRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Delete` | `Boolean` | Optional | If true, prevents the Load Balancer from being deleted | Boolean getDelete() | setDelete(Boolean delete) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.LoadBalancersActionsChangeProtectionRequest;
import java.io.IOException;

LoadBalancersActionsChangeProtectionRequest loadBalancersActionsChangeProtectionRequest = new LoadBalancersActionsChangeProtectionRequest.Builder()
    .delete(true)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



