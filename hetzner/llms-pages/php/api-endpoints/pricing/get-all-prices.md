# Get All Prices

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0ZSUyRlByaWNpbmclMkZHZXQlMjUyMGFsbCUyNTIwcHJpY2Vz

Returns prices for all resources available on the platform. VAT and currency of the Project owner are used for calculations.

Both net and gross prices are included in the response.

:information_source: **Note** This endpoint does not require authentication.

```php
function getAllPrices(): PricingResponse
```


# Response Type

**200**: The `pricing` key in the reply contains an pricing object with this structure

[`PricingResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/pricing-response.md)


# Example Usage

```php
$pricingController = $client->getPricingController();

try {
    $result = $pricingController->getAllPrices();
    echo 'PricingResponse:';
    var_dump($result);
} catch (ApiException $exp) {
    echo 'Caught:', $exp;
}
```



