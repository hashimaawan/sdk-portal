# Get Heartbeat

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/php/x-redirect/JTI0ZSUyRkhlYWx0aCUyRkdldEhlYXJ0YmVhdA

:information_source: **Note** This endpoint does not require authentication.

```php
function getHeartbeat(): ApiResponse
```


# Response Type

**200**: OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type `string`.


# Example Usage

```php
$healthApi = $client->getHealthApi();
$apiResponse = $healthApi->getHeartbeat();

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'string:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```



