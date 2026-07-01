# Get a Load Balancer

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyRkdldCUyNTIwYSUyNTIwTG9hZCUyNTIwQmFsYW5jZXI

Gets a specific Load Balancer object.

:information_source: **Note** This endpoint does not require authentication.

```csharp
GetALoadBalancerAsync(
    int id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Load Balancer |


# Response Type

**200**: The `load_balancer` key contains the Load Balancer

[`Task<Models.LoadBalancersResponse2>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/load-balancers-response-2.md)


# Example Usage

```csharp
int id = 112;
try
{
    LoadBalancersResponse2 result = await loadBalancersController.GetALoadBalancerAsync(id);
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```



