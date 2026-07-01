# Load Balancers Actions Delete Service Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwQWN0aW9ucyUyNTIwRGVsZXRlJTI1MjBTZXJ2aWNlJTI1MjBSZXF1ZXN0


# Class Name

`LoadBalancersActionsDeleteServiceRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ListenPort` | `double` | Required | The listen port of the service you want to delete | double getListenPort() | setListenPort(double listenPort) |


# Example

```java
import cloud.hetzner.api.models.LoadBalancersActionsDeleteServiceRequest;

LoadBalancersActionsDeleteServiceRequest loadBalancersActionsDeleteServiceRequest = new LoadBalancersActionsDeleteServiceRequest.Builder(
    4711D
)
.build();
```



