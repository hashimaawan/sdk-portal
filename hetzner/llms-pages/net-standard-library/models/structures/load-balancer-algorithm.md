# Load Balancer Algorithm

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlckFsZ29yaXRobQ

Algorithm of the Load Balancer


# Class Name

`LoadBalancerAlgorithm`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Type` | [`Type28Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/enumerations/type-28.md) | Required | Type of the algorithm |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

LoadBalancerAlgorithm loadBalancerAlgorithm = new LoadBalancerAlgorithm
{
    Type = Type28Enum.RoundRobin,
};
```



