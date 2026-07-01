# Get All Firewalls

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRkZpcmV3YWxscyUyRkdldCUyNTIwYWxsJTI1MjBGaXJld2FsbHM

Returns all Firewall objects.

:information_source: **Note** This endpoint does not require authentication.

```csharp
GetAllFirewallsAsync(
    Models.Sort? sort = null,
    string name = null,
    string labelSelector = null)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `sort` | [`Sort?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/enumerations/sort.md) | Query, Optional | Can be used multiple times. |
| `name` | `string` | Query, Optional | Can be used to filter resources by their name. The response will only contain the resources matching the specified name |
| `labelSelector` | `string` | Query, Optional | Can be used to filter resources by labels. The response will only contain resources matching the label selector. |


# Response Type

**200**: The `firewalls` key contains an array of Firewall objects

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [Models.FirewallsResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/firewalls-response.md).


# Example Usage

```csharp
try
{
    ApiResponse<FirewallsResponse> result = await firewallsApi.GetAllFirewallsAsync();
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```



