# Load Balancers Actions Attach to Network Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwQWN0aW9ucyUyNTIwQXR0YWNoJTI1MjBUbyUyNTIwTmV0d29yayUyNTIwUmVxdWVzdA


# Class Name

`LoadBalancersActionsAttachToNetworkRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Ip` | `String` | Optional | IP to request to be assigned to this Load Balancer; if you do not provide this then you will be auto assigned an IP address | String getIp() | setIp(String ip) |
| `Network` | `double` | Required | ID of an existing network to attach the Load Balancer to | double getNetwork() | setNetwork(double network) |


# Example

```java
import cloud.hetzner.api.models.LoadBalancersActionsAttachToNetworkRequest;

LoadBalancersActionsAttachToNetworkRequest loadBalancersActionsAttachToNetworkRequest = new LoadBalancersActionsAttachToNetworkRequest.Builder(
    4711D
)
.ip("10.0.1.1")
.build();
```



