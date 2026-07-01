# Load Balancers Actions Attach to Network Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwQWN0aW9ucyUyNTIwQXR0YWNoJTI1MjBUbyUyNTIwTmV0d29yayUyNTIwUmVxdWVzdA

*This model accepts additional fields of type object.*


# Class Name

`LoadBalancersActionsAttachToNetworkRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Ip` | `string` | Optional | IP to request to be assigned to this Load Balancer; if you do not provide this then you will be auto assigned an IP address |
| `Network` | `double` | Required | ID of an existing network to attach the Load Balancer to |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;

LoadBalancersActionsAttachToNetworkRequest loadBalancersActionsAttachToNetworkRequest = new LoadBalancersActionsAttachToNetworkRequest
{
    Network = 4711,
    Ip = "10.0.1.1",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



