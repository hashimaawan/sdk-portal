# Load Balancer Algorithm

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlckFsZ29yaXRobQ

Algorithm of the Load Balancer

*This model accepts additional fields of type object.*


# Class Name

`LoadBalancerAlgorithm`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Type` | [`Type28`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/enumerations/type-28.md) | Required | Type of the algorithm |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;

LoadBalancerAlgorithm loadBalancerAlgorithm = new LoadBalancerAlgorithm
{
    Type = Type28.RoundRobin,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



