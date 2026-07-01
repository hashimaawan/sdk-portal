# Get All Prices

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0ZSUyRlByaWNpbmclMkZHZXQlMjUyMGFsbCUyNTIwcHJpY2Vz

Returns prices for all resources available on the platform. VAT and currency of the Project owner are used for calculations.

Both net and gross prices are included in the response.

:information_source: **Note** This endpoint does not require authentication.

```php
function getAllPrices(): ApiResponse
```


# Response Type

**200**: The `pricing` key in the reply contains an pricing object with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`PricingResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/pricing-response.md).


# Example Usage

```php
$pricingApi = $client->getPricingApi();
$apiResponse = $pricingApi->getAllPrices();

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'PricingResponse:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```



