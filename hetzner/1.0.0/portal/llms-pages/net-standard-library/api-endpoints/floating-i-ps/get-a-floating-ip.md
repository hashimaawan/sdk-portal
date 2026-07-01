# Get a Floating IP

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRkZsb2F0aW5nJTI1MjBJUHMlMkZHZXQlMjUyMGElMjUyMEZsb2F0aW5nJTI1MjBJUA

Returns a specific Floating IP object.

:information_source: **Note** This endpoint does not require authentication.

```csharp
GetAFloatingIpAsync(
    int id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Floating IP |


# Response Type

**200**: The `floating_ip` key in the reply contains a Floating IP object with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [Models.FloatingIpsResponse2](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/floating-ips-response-2.md).


# Example Usage

```csharp
int id = 112;
try
{
    ApiResponse<FloatingIpsResponse2> result = await floatingIPsApi.GetAFloatingIpAsync(id);
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```



