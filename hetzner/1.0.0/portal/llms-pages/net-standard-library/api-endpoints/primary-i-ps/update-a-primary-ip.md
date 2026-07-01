# Update a Primary IP

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRlByaW1hcnklMjUyMElQcyUyRlVwZGF0ZSUyNTIwYSUyNTIwUHJpbWFyeSUyNTIwSVA

Updates the Primary IP.

Note that when updating labels, the Primary IP's current set of labels will be replaced with the labels provided in the request body. So, for example, if you want to add a new label, you have to provide all existing labels plus the new label in the request body.

If the Primary IP object changes during the request, the response will be a “conflict” error.

:information_source: **Note** This endpoint does not require authentication.

```csharp
UpdateAPrimaryIpAsync(
    int id,
    Models.UpdatePrimaryIpRequest body = null)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the resource |
| `body` | [`UpdatePrimaryIpRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/update-primary-ip-request.md) | Body, Optional | - |


# Response Type

**200**: The `primary_ip` key contains the Primary IP that was just updated

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [Models.PrimaryIpResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/primary-ip-response.md).


# Example Usage

```csharp
int id = 112;
UpdatePrimaryIpRequest body = new UpdatePrimaryIpRequest
{
    AutoDelete = true,
    Labels = ApiHelper.JsonDeserialize<object>("{\"labelkey\":\"value\"}"),
    Name = "my-ip",
};

try
{
    ApiResponse<PrimaryIpResponse> result = await primaryIPsApi.UpdateAPrimaryIpAsync(
        id,
        body
    );
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```



