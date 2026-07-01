# Search Gifs

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/java/x-redirect/JTI0ZSUyRmdpZnMlMkZzZWFyY2hHaWZz

Search all GIPHY GIFs for a word or phrase. Punctuation will be stripped and ignored.  Use a plus or url encode for phrases. Example paul+rudd, ryan+gosling or american+psycho.

```java
CompletableFuture<ApiResponse<GifsSearchResponse>> searchGifsAsync(
    final String q,
    final Integer limit,
    final Integer offset,
    final String rating,
    final String lang)
```


# Authentication

This endpoint requires [api_key](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/java/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `q` | `String` | Query, Required | Search query term or prhase. |
| `limit` | `Integer` | Query, Optional | The maximum number of records to return.<br><br>**Default**: `25` |
| `offset` | `Integer` | Query, Optional | An optional results offset.<br><br>**Default**: `0` |
| `rating` | `String` | Query, Optional | Filters results by specified rating. |
| `lang` | `String` | Query, Optional | Specify default language for regional content; use a 2-letter ISO 639-1 language code. |


# Response Type

**200**: Search results

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`GifsSearchResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/java/models/structures/gifs-search-response.md).


# Example Usage

```java
String q = "q0";
Integer limit = 25;
Integer offset = 0;

gifsApi.searchGifsAsync(q, limit, offset, null, null).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Your request was formatted incorrectly or missing required parameters. | `ApiException` |
| 403 | You weren't authorized to make your request; most likely this indicates an issue with your API Key. | `ApiException` |
| 404 | The particular GIF you are requesting was not found. This occurs, for example, if you request a GIF by an id that does not exist. | `ApiException` |
| 429 | Your API Key is making too many requests. Read about [requesting a Production Key](https://developers.giphy.com/docs/#access) to upgrade your API Key rate limits. | `ApiException` |



