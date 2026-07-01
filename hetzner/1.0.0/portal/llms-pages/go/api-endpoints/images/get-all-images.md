# Get All Images

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0ZSUyRkltYWdlcyUyRkdldCUyNTIwYWxsJTI1MjBJbWFnZXM

Returns all Image objects. You can select specific Image types only and sort the results by using URI parameters.

:information_source: **Note** This endpoint does not require authentication.

```go
GetAllImages(
    ctx context.Context,
    sort *models.Sort,
    mType *models.Type21,
    status *models.Status23,
    boundTo *string,
    includeDeprecated *bool,
    name *string,
    labelSelector *string) (
    models.ApiResponse[models.ImagesResponse],
    error)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `sort` | [`*models.Sort`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/enumerations/sort.md) | Query, Optional | Can be used multiple times. |
| `mType` | [`*models.Type21`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/enumerations/type-21.md) | Query, Optional | Can be used multiple times. |
| `status` | [`*models.Status23`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/enumerations/status-23.md) | Query, Optional | Can be used multiple times. The response will only contain Images matching the status. |
| `boundTo` | `*string` | Query, Optional | Can be used multiple times. Server ID linked to the Image. Only available for Images of type `backup` |
| `includeDeprecated` | `*bool` | Query, Optional | Can be used multiple times. |
| `name` | `*string` | Query, Optional | Can be used to filter resources by their name. The response will only contain the resources matching the specified name |
| `labelSelector` | `*string` | Query, Optional | Can be used to filter resources by labels. The response will only contain resources matching the label selector. |


# Response Type

**200**: The `images` key in the reply contains an array of Image objects with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.ImagesResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/images-response.md).


# Example Usage

```go
ctx := context.Background()

apiResponse, err := imagesApi.GetAllImages(ctx, nil, nil, nil, nil, nil, nil, nil)
if err != nil {
    log.Fatalln(err)
} else {
    // Printing the result and response
    fmt.Println(apiResponse.Data)
    fmt.Println(apiResponse.Response.StatusCode)
}
```



