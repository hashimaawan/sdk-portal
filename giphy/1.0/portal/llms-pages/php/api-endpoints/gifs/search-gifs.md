# Search Gifs

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/php/x-redirect/JTI0ZSUyRmdpZnMlMkZzZWFyY2hHaWZz

Search all GIPHY GIFs for a word or phrase. Punctuation will be stripped and ignored.  Use a plus or url encode for phrases. Example paul+rudd, ryan+gosling or american+psycho.

```php
function searchGifs(
    string $q,
    ?int $limit = 25,
    ?int $offset = 0,
    ?string $rating = null,
    ?string $lang = null
): ApiResponse
```


# Authentication

This endpoint requires [api_key](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/php/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `q` | `string` | Query, Required | Search query term or prhase. |
| `limit` | `?int` | Query, Optional | The maximum number of records to return.<br><br>**Default**: `25` |
| `offset` | `?int` | Query, Optional | An optional results offset.<br><br>**Default**: `0` |
| `rating` | `?string` | Query, Optional | Filters results by specified rating. |
| `lang` | `?string` | Query, Optional | Specify default language for regional content; use a 2-letter ISO 639-1 language code. |


# Response Type

**200**: Search results

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`GifsSearchResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/php/models/structures/gifs-search-response.md).


# Example Usage

```php
$q = 'q0';

$limit = 25;

$offset = 0;

$gifsApi = $client->getGifsApi();
$apiResponse = $gifsApi->searchGifs(
    $q,
    $limit,
    $offset
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'GifsSearchResponse:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Your request was formatted incorrectly or missing required parameters. | `ApiException` |
| 403 | You weren't authorized to make your request; most likely this indicates an issue with your API Key. | `ApiException` |
| 404 | The particular GIF you are requesting was not found. This occurs, for example, if you request a GIF by an id that does not exist. | `ApiException` |
| 429 | Your API Key is making too many requests. Read about [requesting a Production Key](https://developers.giphy.com/docs/#access) to upgrade your API Key rate limits. | `ApiException` |



