# Delete a Load Balancer

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyRkRlbGV0ZSUyNTIwYSUyNTIwTG9hZCUyNTIwQmFsYW5jZXI

Deletes a Load Balancer.

:information_source: **Note** This endpoint does not require authentication.

```csharp
DeleteALoadBalancerAsync(
    int id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Load Balancer |


# Response Type

**204**: Load Balancer deleted

`Task`


# Example Usage

```csharp
int id = 112;
try
{
    await loadBalancersApi.DeleteALoadBalancerAsync(id);
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```



