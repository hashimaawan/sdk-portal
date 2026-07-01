# Get a Primary IP

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRlByaW1hcnklMjUyMElQcyUyRkdldCUyNTIwYSUyNTIwUHJpbWFyeSUyNTIwSVA

Returns a specific Primary IP object.

:information_source: **Note** This endpoint does not require authentication.

```csharp
GetAPrimaryIpAsync(
    int id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the resource |


# Response Type

**200**: The `primary_ip` key contains a Primary IP object

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [Models.PrimaryIpResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/primary-ip-response.md).


# Example Usage

```csharp
int id = 112;
try
{
    ApiResponse<PrimaryIpResponse> result = await primaryIPsApi.GetAPrimaryIpAsync(id);
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```



