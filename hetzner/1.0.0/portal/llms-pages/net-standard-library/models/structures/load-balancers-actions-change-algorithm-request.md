# Load Balancers Actions Change Algorithm Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwQWN0aW9ucyUyNTIwQ2hhbmdlJTI1MjBBbGdvcml0aG0lMjUyMFJlcXVlc3Q


# Class Name

`LoadBalancersActionsChangeAlgorithmRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Type` | [`Type39Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/enumerations/type-39.md) | Required | Algorithm of the Load Balancer |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

LoadBalancersActionsChangeAlgorithmRequest loadBalancersActionsChangeAlgorithmRequest = new LoadBalancersActionsChangeAlgorithmRequest
{
    Type = Type39Enum.RoundRobin,
};
```



