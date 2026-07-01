# Load Balancers Actions Change Algorithm Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwQWN0aW9ucyUyNTIwQ2hhbmdlJTI1MjBBbGdvcml0aG0lMjUyMFJlcXVlc3Q

*This model accepts additional fields of type object.*


# Class Name

`LoadBalancersActionsChangeAlgorithmRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Type` | [`Type39`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/enumerations/type-39.md) | Required | Algorithm of the Load Balancer |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;

LoadBalancersActionsChangeAlgorithmRequest loadBalancersActionsChangeAlgorithmRequest = new LoadBalancersActionsChangeAlgorithmRequest
{
    Type = Type39.RoundRobin,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



