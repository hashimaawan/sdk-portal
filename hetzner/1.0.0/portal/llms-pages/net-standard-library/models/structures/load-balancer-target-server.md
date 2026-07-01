# Load Balancer Target Server

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclRhcmdldFNlcnZlcg

Server where the traffic should be routed through

*This model accepts additional fields of type object.*


# Class Name

`LoadBalancerTargetServer`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Id` | `int` | Required | ID of the Server |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;

LoadBalancerTargetServer loadBalancerTargetServer = new LoadBalancerTargetServer
{
    Id = 80,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



