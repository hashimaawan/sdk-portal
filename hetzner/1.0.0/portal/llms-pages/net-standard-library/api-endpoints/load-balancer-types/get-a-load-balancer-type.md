# Get a Load Balancer Type

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRkxvYWQlMjUyMEJhbGFuY2VyJTI1MjBUeXBlcyUyRkdldCUyNTIwYSUyNTIwTG9hZCUyNTIwQmFsYW5jZXIlMjUyMFR5cGU

Gets a specific Load Balancer type object.

:information_source: **Note** This endpoint does not require authentication.

```csharp
GetALoadBalancerTypeAsync(
    int id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of Load Balancer type |


# Response Type

**200**: The `load_balancer_type` key in the reply contains a Load Balancer type object with this structure

[`Task<Models.LoadBalancerTypesResponse1>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/load-balancer-types-response-1.md)


# Example Usage

```csharp
int id = 112;
try
{
    LoadBalancerTypesResponse1 result = await loadBalancerTypesController.GetALoadBalancerTypeAsync(id);
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```



