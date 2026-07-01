# Delete a Server

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRlNlcnZlcnMlMkZEZWxldGUlMjUyMGElMjUyMFNlcnZlcg

Deletes a Server. This immediately removes the Server from your account, and it is no longer accessible.

:information_source: **Note** This endpoint does not require authentication.

```csharp
DeleteAServerAsync(
    int id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Server |


# Response Type

**200**: The `action` key in the reply contains an Action object with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [Models.ServersResponse1](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/servers-response-1.md).


# Example Usage

```csharp
int id = 112;
try
{
    ApiResponse<ServersResponse1> result = await serversApi.DeleteAServerAsync(id);
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```



