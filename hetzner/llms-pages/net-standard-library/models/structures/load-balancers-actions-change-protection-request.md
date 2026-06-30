# Load Balancers Actions Change Protection Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwQWN0aW9ucyUyNTIwQ2hhbmdlJTI1MjBQcm90ZWN0aW9uJTI1MjBSZXF1ZXN0


# Class Name

`LoadBalancersActionsChangeProtectionRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Delete` | `bool?` | Optional | If true, prevents the Load Balancer from being deleted |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

LoadBalancersActionsChangeProtectionRequest loadBalancersActionsChangeProtectionRequest = new LoadBalancersActionsChangeProtectionRequest
{
    Delete = true,
};
```



