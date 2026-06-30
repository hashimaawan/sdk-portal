# Delete a Firewall

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0ZSUyRkZpcmV3YWxscyUyRkRlbGV0ZSUyNTIwYSUyNTIwRmlyZXdhbGw

Deletes a Firewall.

#### Call specific error codes

| Code                 | Description                               |
|--------------------- |-------------------------------------------|
| `resource_in_use`    | Firewall must not be in use to be deleted |

:information_source: **Note** This endpoint does not require authentication.

```csharp
DeleteAFirewallAsync(
    int id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the resource |


# Response Type

**204**: Firewall deleted

`Task`


# Example Usage

```csharp
int id = 112;
try
{
    await firewallsController.DeleteAFirewallAsync(id);
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```



