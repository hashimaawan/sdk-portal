# Get Gifs by Id

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/#/php/x-redirect/JTI0ZSUyRmdpZnMlMkZnZXRHaWZzQnlJZA

A multiget version of the get GIF by ID endpoint.

```php
function getGifsById(?string $ids = null): GifsResponse
```


# Authentication

This endpoint requires [api_key](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/php/getting-started/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ids` | `?string` | Query, Optional | Filters results by specified GIF IDs, separated by commas. |


# Response Type

**200**

[`GifsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/php/models/structures/gifs-response.md)


# Example Usage

```php
$gifsController = $client->getGifsController();

try {
    $result = $gifsController->getGifsById();
    echo 'GifsResponse:';
    var_dump($result);
} catch (ApiException $exp) {
    echo 'Caught:', $exp;
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Your request was formatted incorrectly or missing required parameters. | `ApiException` |
| 403 | You weren't authorized to make your request; most likely this indicates an issue with your API Key. | `ApiException` |
| 404 | The particular GIF you are requesting was not found. This occurs, for example, if you request a GIF by an id that does not exist. | `ApiException` |
| 429 | Your API Key is making too many requests. Read about [requesting a Production Key](https://developers.giphy.com/docs/#access) to upgrade your API Key rate limits. | `ApiException` |



