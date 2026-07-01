# Get an Image

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRkltYWdlcyUyRkdldCUyNTIwYW4lMjUyMEltYWdl

Returns a specific Image object.

:information_source: **Note** This endpoint does not require authentication.

```csharp
GetAnImageAsync(
    int id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Image |


# Response Type

**200**: The `image` key in the reply contains an Image object with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [Models.ImagesResponse1](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/images-response-1.md).


# Example Usage

```csharp
int id = 112;
try
{
    ApiResponse<ImagesResponse1> result = await imagesApi.GetAnImageAsync(id);
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```



