# Translate Gif

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/#/go/x-redirect/JTI0ZSUyRmdpZnMlMkZ0cmFuc2xhdGVHaWY

The translate API draws on search, but uses the GIPHY `special sauce` to handle translating from one vocabulary to another. In this case, words and phrases to GIF

```go
TranslateGif(
    ctx context.Context,
    s string) (
    models.ApiResponse[models.GifsTranslateResponse],
    error)
```


# Authentication

This endpoint requires [api_key](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/go/getting-started/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `s` | `string` | Query, Required | Search term. |


# Response Type

**200**

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.GifsTranslateResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/go/models/structures/gifs-translate-response.md).


# Example Usage

```go
ctx := context.Background()

s := "s8"

apiResponse, err := gifsController.TranslateGif(ctx, s)
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



