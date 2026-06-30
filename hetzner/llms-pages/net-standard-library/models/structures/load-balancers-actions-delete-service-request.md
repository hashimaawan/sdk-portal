# Load Balancers Actions Delete Service Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwQWN0aW9ucyUyNTIwRGVsZXRlJTI1MjBTZXJ2aWNlJTI1MjBSZXF1ZXN0


# Class Name

`LoadBalancersActionsDeleteServiceRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ListenPort` | `double` | Required | The listen port of the service you want to delete |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

LoadBalancersActionsDeleteServiceRequest loadBalancersActionsDeleteServiceRequest = new LoadBalancersActionsDeleteServiceRequest
{
    ListenPort = 4711,
};
```



