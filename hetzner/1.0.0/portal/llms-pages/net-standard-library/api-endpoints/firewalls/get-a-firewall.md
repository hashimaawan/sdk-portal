# Get a Firewall

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRkZpcmV3YWxscyUyRkdldCUyNTIwYSUyNTIwRmlyZXdhbGw

Gets a specific Firewall object.

:information_source: **Note** This endpoint does not require authentication.

```csharp
GetAFirewallAsync(
    int id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the resource |


# Response Type

**200**: The `firewall` key contains a Firewall object

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [Models.FirewallResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/firewall-response.md).


# Example Usage

```csharp
int id = 112;
try
{
    ApiResponse<FirewallResponse> result = await firewallsApi.GetAFirewallAsync(id);
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```



