# Random Sticker

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/go/x-redirect/JTI0ZSUyRnN0aWNrZXJzJTJGcmFuZG9tU3RpY2tlcg

Returns a random GIF, limited by tag. Excluding the tag parameter will return a random GIF from the GIPHY catalog.

```go
RandomSticker(
    ctx context.Context,
    tag *string,
    rating *string) (
    models.ApiResponse[models.StickersRandomResponse],
    error)
```


# Authentication

This endpoint requires [api_key](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/go/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `tag` | `*string` | Query, Optional | Filters results by specified tag. |
| `rating` | `*string` | Query, Optional | Filters results by specified rating. |


# Response Type

**200**

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.StickersRandomResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/go/models/structures/stickers-random-response.md).


# Example Usage

```go
ctx := context.Background()

apiResponse, err := stickersApi.RandomSticker(ctx, nil, nil)
if err != nil {
    log.Fatalln(err)
} else {
    // Printing the result and response
    fmt.Println(apiResponse.Data)
    fmt.Println(apiResponse.Response.StatusCode)
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Your request was formatted incorrectly or missing required parameters. | `ApiError` |
| 403 | You weren't authorized to make your request; most likely this indicates an issue with your API Key. | `ApiError` |
| 404 | The particular GIF you are requesting was not found. This occurs, for example, if you request a GIF by an id that does not exist. | `ApiError` |
| 429 | Your API Key is making too many requests. Read about [requesting a Production Key](https://developers.giphy.com/docs/#access) to upgrade your API Key rate limits. | `ApiError` |



