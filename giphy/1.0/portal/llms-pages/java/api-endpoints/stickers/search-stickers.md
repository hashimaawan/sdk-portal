# Search Stickers

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/java/x-redirect/JTI0ZSUyRnN0aWNrZXJzJTJGc2VhcmNoU3RpY2tlcnM

Replicates the functionality and requirements of the classic GIPHY search, but returns animated stickers rather than GIFs.

```java
CompletableFuture<StickersSearchResponse> searchStickersAsync(
    final String q,
    final Integer limit,
    final Integer offset,
    final String rating,
    final String lang)
```


# Authentication

This endpoint requires [api_key](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/java/getting-started/authorization.md)


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

[`StickersSearchResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/java/models/structures/stickers-search-response.md)


# Example Usage

```java
String q = "q0";
Integer limit = 25;
Integer offset = 0;

stickersController.searchStickersAsync(q, limit, offset, null, null).thenAccept(result -> {
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



