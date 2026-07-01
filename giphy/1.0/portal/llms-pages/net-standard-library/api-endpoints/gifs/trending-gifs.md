# Trending Gifs

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRmdpZnMlMkZ0cmVuZGluZ0dpZnM

Fetch GIFs currently trending online. Hand curated by the GIPHY editorial team.  The data returned mirrors the GIFs showcased on the GIPHY homepage. Returns 25 results by default.

```csharp
TrendingGifsAsync(
    int? limit = 25,
    int? offset = 0,
    string rating = null)
```


# Authentication

This endpoint requires [api_key](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/net-standard-library/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `limit` | `int?` | Query, Optional | The maximum number of records to return.<br><br>**Default**: `25` |
| `offset` | `int?` | Query, Optional | An optional results offset.<br><br>**Default**: `0` |
| `rating` | `string` | Query, Optional | Filters results by specified rating. |


# Response Type

**200**

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/net-standard-library/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [Models.GifsTrendingResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/net-standard-library/models/structures/gifs-trending-response.md).


# Example Usage

```csharp
int? limit = 25;
int? offset = 0;
try
{
    ApiResponse<GifsTrendingResponse> result = await gifsApi.TrendingGifsAsync(
        limit,
        offset
    );
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Your request was formatted incorrectly or missing required parameters. | `ApiException` |
| 403 | You weren't authorized to make your request; most likely this indicates an issue with your API Key. | `ApiException` |
| 404 | The particular GIF you are requesting was not found. This occurs, for example, if you request a GIF by an id that does not exist. | `ApiException` |
| 429 | Your API Key is making too many requests. Read about [requesting a Production Key](https://developers.giphy.com/docs/#access) to upgrade your API Key rate limits. | `ApiException` |



