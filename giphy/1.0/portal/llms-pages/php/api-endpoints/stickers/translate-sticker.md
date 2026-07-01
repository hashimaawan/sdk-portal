# Translate Sticker

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/php/x-redirect/JTI0ZSUyRnN0aWNrZXJzJTJGdHJhbnNsYXRlU3RpY2tlcg

The translate API draws on search, but uses the GIPHY `special sauce` to handle translating from one vocabulary to another. In this case, words and phrases to GIFs.

```php
function translateSticker(string $s): ApiResponse
```


# Authentication

This endpoint requires [api_key](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/php/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `s` | `string` | Query, Required | Search term. |


# Response Type

**200**

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`StickersTranslateResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/php/models/structures/stickers-translate-response.md).


# Example Usage

```php
$s = 's8';

$stickersApi = $client->getStickersApi();
$apiResponse = $stickersApi->translateSticker($s);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'StickersTranslateResponse:';
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



