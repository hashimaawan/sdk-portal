# Trending Stickers

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/#/go/x-redirect/JTI0ZSUyRnN0aWNrZXJzJTJGdHJlbmRpbmdTdGlja2Vycw

Fetch Stickers currently trending online. Hand curated by the GIPHY editorial team. Returns 25 results by default.

```go
TrendingStickers(
    ctx context.Context,
    limit *int,
    offset *int,
    rating *string) (
    models.ApiResponse[models.StickersTrendingResponse],
    error)
```


# Authentication

This endpoint requires [api_key](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/go/getting-started/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `limit` | `*int` | Query, Optional | The maximum number of records to return.<br><br>**Default**: `25` |
| `offset` | `*int` | Query, Optional | An optional results offset.<br><br>**Default**: `0` |
| `rating` | `*string` | Query, Optional | Filters results by specified rating. |


# Response Type

**200**

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.StickersTrendingResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/go/models/structures/stickers-trending-response.md).


# Example Usage

```go
ctx := context.Background()

limit := 25

offset := 0

apiResponse, err := stickersController.TrendingStickers(ctx, &limit, &offset, nil)
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



