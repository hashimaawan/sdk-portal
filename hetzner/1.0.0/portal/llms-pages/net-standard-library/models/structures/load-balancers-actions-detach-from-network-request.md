# Load Balancers Actions Detach from Network Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwQWN0aW9ucyUyNTIwRGV0YWNoJTI1MjBGcm9tJTI1MjBOZXR3b3JrJTI1MjBSZXF1ZXN0


# Class Name

`LoadBalancersActionsDetachFromNetworkRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Network` | `double` | Required | ID of an existing network to detach the Load Balancer from |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

LoadBalancersActionsDetachFromNetworkRequest loadBalancersActionsDetachFromNetworkRequest = new LoadBalancersActionsDetachFromNetworkRequest
{
    Network = 4711,
};
```



