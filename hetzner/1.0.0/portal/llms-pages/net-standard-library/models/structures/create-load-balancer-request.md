# Create Load Balancer Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkNyZWF0ZUxvYWRCYWxhbmNlclJlcXVlc3Q


# Class Name

`CreateLoadBalancerRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Algorithm` | [`LoadBalancerAlgorithm`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/load-balancer-algorithm.md) | Required | Algorithm of the Load Balancer |
| `Labels` | [`Labels`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/labels.md) | Optional | User-defined labels (key-value pairs) |
| `LoadBalancerType` | `string` | Required | ID or name of the Load Balancer type this Load Balancer should be created with |
| `Location` | `string` | Optional | ID or name of Location to create Load Balancer in |
| `Name` | `string` | Required | Name of the Load Balancer |
| `Network` | `int?` | Optional | ID of the network the Load Balancer should be attached to on creation |
| `NetworkZone` | `string` | Optional | Name of network zone |
| `PublicInterface` | `bool?` | Optional | Enable or disable the public interface of the Load Balancer |
| `Services` | [`List<LoadBalancerService>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/load-balancer-service.md) | Optional | Array of services |
| `Targets` | [`List<LoadBalancerTarget>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/load-balancer-target.md) | Optional | Array of targets |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

CreateLoadBalancerRequest createLoadBalancerRequest = new CreateLoadBalancerRequest
{
    Algorithm = new LoadBalancerAlgorithm
    {
        Type = Type28Enum.RoundRobin,
    },
    LoadBalancerType = "lb11",
    Name = "Web Frontend",
    Labels = new Labels
    {
        Labelkey = "labelkey4",
    },
    Location = "location2",
    Network = 123,
    NetworkZone = "eu-central",
    PublicInterface = true,
};
```



