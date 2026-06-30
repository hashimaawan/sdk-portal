# Search Gifs

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/#/net-standard-library/x-redirect/JTI0ZSUyRmdpZnMlMkZzZWFyY2hHaWZz

Search all GIPHY GIFs for a word or phrase. Punctuation will be stripped and ignored.  Use a plus or url encode for phrases. Example paul+rudd, ryan+gosling or american+psycho.

```csharp
SearchGifsAsync(
    string q,
    int? limit = 25,
    int? offset = 0,
    string rating = null,
    string lang = null)
```


# Authentication

This endpoint requires [api_key](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/net-standard-library/getting-started/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `q` | `string` | Query, Required | Search query term or prhase. |
| `limit` | `int?` | Query, Optional | The maximum number of records to return.<br><br>**Default**: `25` |
| `offset` | `int?` | Query, Optional | An optional results offset.<br><br>**Default**: `0` |
| `rating` | `string` | Query, Optional | Filters results by specified rating. |
| `lang` | `string` | Query, Optional | Specify default language for regional content; use a 2-letter ISO 639-1 language code. |


# Response Type

**200**: Search results

[`Task<Models.GifsSearchResponse>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/net-standard-library/models/structures/gifs-search-response.md)


# Example Usage

```csharp
string q = "q0";
int? limit = 25;
int? offset = 0;
try
{
    GifsSearchResponse result = await gifsController.SearchGifsAsync(
        q,
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



