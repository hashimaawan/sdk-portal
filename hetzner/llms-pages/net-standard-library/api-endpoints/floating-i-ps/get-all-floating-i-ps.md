# Get All Floating I Ps

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0ZSUyRkZsb2F0aW5nJTI1MjBJUHMlMkZHZXQlMjUyMGFsbCUyNTIwRmxvYXRpbmclMjUyMElQcw

Returns all Floating IP objects.

:information_source: **Note** This endpoint does not require authentication.

```csharp
GetAllFloatingIPsAsync(
    string name = null,
    string labelSelector = null,
    Models.Sort2Enum? sort = null)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `string` | Query, Optional | Can be used to filter Floating IPs by their name. The response will only contain the Floating IP matching the specified name. |
| `labelSelector` | `string` | Query, Optional | Can be used to filter Floating IPs by labels. The response will only contain Floating IPs matching the label selector. |
| `sort` | [`Sort2Enum?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/enumerations/sort-2.md) | Query, Optional | Can be used multiple times. Choices id id:asc id:desc created created:asc created:desc |


# Response Type

**200**: The `floating_ips` key in the reply contains an array of Floating IP objects with this structure

[`Task<Models.FloatingIpsResponse>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/floating-ips-response.md)


# Example Usage

```csharp
try
{
    FloatingIpsResponse result = await floatingIPsController.GetAllFloatingIPsAsync();
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```



