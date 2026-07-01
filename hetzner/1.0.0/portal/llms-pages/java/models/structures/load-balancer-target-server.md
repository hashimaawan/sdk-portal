# Load Balancer Target Server

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclRhcmdldFNlcnZlcg

Server where the traffic should be routed through


# Class Name

`LoadBalancerTargetServer`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `int` | Required | ID of the Server | int getId() | setId(int id) |


# Example

```java
import cloud.hetzner.api.models.LoadBalancerTargetServer;

LoadBalancerTargetServer loadBalancerTargetServer = new LoadBalancerTargetServer.Builder(
    80
)
.build();
```



