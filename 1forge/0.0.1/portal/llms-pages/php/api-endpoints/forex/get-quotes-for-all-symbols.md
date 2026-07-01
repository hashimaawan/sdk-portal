# Get Quotes for All Symbols

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1forge/0.0.1/portal/#/php/x-redirect/JTI0ZSUyRmZvcmV4JTJGR2V0JTI1MjBxdW90ZXMlMjUyMGZvciUyNTIwYWxsJTI1MjBzeW1ib2xz

Get quotes

Find out more: [http://1forge.com/forex-data-api](http://1forge.com/forex-data-api)

:information_source: **Note** This endpoint does not require authentication.

```php
function getQuotesForAllSymbols(): ApiResponse
```


# Response Type

**200**: A list of quotes

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1forge/0.0.1/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```php
$forexApi = $client->getForexApi();
$apiResponse = $forexApi->getQuotesForAllSymbols();

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'void:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```



