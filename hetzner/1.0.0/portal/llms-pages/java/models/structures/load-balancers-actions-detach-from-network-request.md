# Load Balancers Actions Detach from Network Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwQWN0aW9ucyUyNTIwRGV0YWNoJTI1MjBGcm9tJTI1MjBOZXR3b3JrJTI1MjBSZXF1ZXN0


# Class Name

`LoadBalancersActionsDetachFromNetworkRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Network` | `double` | Required | ID of an existing network to detach the Load Balancer from | double getNetwork() | setNetwork(double network) |


# Example

```java
import cloud.hetzner.api.models.LoadBalancersActionsDetachFromNetworkRequest;

LoadBalancersActionsDetachFromNetworkRequest loadBalancersActionsDetachFromNetworkRequest = new LoadBalancersActionsDetachFromNetworkRequest.Builder(
    4711D
)
.build();
```



