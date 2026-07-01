# Get a List of Symbols for Which We Provide Real-Time Quotes

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1forge/0.0.1/portal/#/php/x-redirect/JTI0ZSUyRmZvcmV4JTJGR2V0JTI1MjBhJTI1MjBsaXN0JTI1MjBvZiUyNTIwc3ltYm9scyUyNTIwZm9yJTI1MjB3aGljaCUyNTIwd2UlMjUyMHByb3ZpZGUlMjUyMHJlYWwtdGltZSUyNTIwcXVvdGVz

Symbol List

Find out more: [http://1forge.com/forex-data-api](http://1forge.com/forex-data-api)

:information_source: **Note** This endpoint does not require authentication.

```php
function getAListOfSymbolsForWhichWeProvideRealTimeQuotes(): ApiResponse
```


# Response Type

**200**: A list of symbols

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1forge/0.0.1/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type `string[]`.


# Example Usage

```php
$forexApi = $client->getForexApi();
$apiResponse = $forexApi->getAListOfSymbolsForWhichWeProvideRealTimeQuotes();

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'string[]:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```



