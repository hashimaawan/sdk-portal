# Get All Images

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRkltYWdlcyUyRkdldCUyNTIwYWxsJTI1MjBJbWFnZXM

Returns all Image objects. You can select specific Image types only and sort the results by using URI parameters.

:information_source: **Note** This endpoint does not require authentication.

```csharp
GetAllImagesAsync(
    Models.Sort? sort = null,
    Models.Type21? type = null,
    Models.Status23? status = null,
    string boundTo = null,
    bool? includeDeprecated = null,
    string name = null,
    string labelSelector = null)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `sort` | [`Sort?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/enumerations/sort.md) | Query, Optional | Can be used multiple times. |
| `type` | [`Type21?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/enumerations/type-21.md) | Query, Optional | Can be used multiple times. |
| `status` | [`Status23?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/enumerations/status-23.md) | Query, Optional | Can be used multiple times. The response will only contain Images matching the status. |
| `boundTo` | `string` | Query, Optional | Can be used multiple times. Server ID linked to the Image. Only available for Images of type `backup` |
| `includeDeprecated` | `bool?` | Query, Optional | Can be used multiple times. |
| `name` | `string` | Query, Optional | Can be used to filter resources by their name. The response will only contain the resources matching the specified name |
| `labelSelector` | `string` | Query, Optional | Can be used to filter resources by labels. The response will only contain resources matching the label selector. |


# Response Type

**200**: The `images` key in the reply contains an array of Image objects with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [Models.ImagesResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/images-response.md).


# Example Usage

```csharp
try
{
    ApiResponse<ImagesResponse> result = await imagesApi.GetAllImagesAsync();
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```



