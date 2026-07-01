# Load Balancers Actions Change Protection Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwQWN0aW9ucyUyNTIwQ2hhbmdlJTI1MjBQcm90ZWN0aW9uJTI1MjBSZXF1ZXN0


# Class Name

`LoadBalancersActionsChangeProtectionRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Delete` | `Boolean` | Optional | If true, prevents the Load Balancer from being deleted | Boolean getDelete() | setDelete(Boolean delete) |


# Example

```java
import cloud.hetzner.api.models.LoadBalancersActionsChangeProtectionRequest;

LoadBalancersActionsChangeProtectionRequest loadBalancersActionsChangeProtectionRequest = new LoadBalancersActionsChangeProtectionRequest.Builder()
    .delete(true)
    .build();
```



