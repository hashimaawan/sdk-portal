# Update a Server

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRlNlcnZlcnMlMkZVcGRhdGUlMjUyMGElMjUyMFNlcnZlcg

Updates a Server. You can update a Server’s name and a Server’s labels.
Please note that Server names must be unique per Project and valid hostnames as per RFC 1123 (i.e. may only contain letters, digits, periods, and dashes).
Also note that when updating labels, the Server’s current set of labels will be replaced with the labels provided in the request body. So, for example, if you want to add a new label, you have to provide all existing labels plus the new label in the request body.

:information_source: **Note** This endpoint does not require authentication.

```csharp
UpdateAServerAsync(
    int id,
    Models.UpdateServerRequest body = null)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Server |
| `body` | [`UpdateServerRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/update-server-request.md) | Body, Optional | - |


# Response Type

**200**: The `server` key in the reply contains the updated Server

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [Models.ServersResponse2](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/servers-response-2.md).


# Example Usage

```csharp
int id = 112;
UpdateServerRequest body = new UpdateServerRequest
{
    Labels = ApiHelper.JsonDeserialize<object>("{\"labelkey\":\"value\"}"),
    Name = "my-server",
};

try
{
    ApiResponse<ServersResponse2> result = await serversApi.UpdateAServerAsync(
        id,
        body
    );
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```



