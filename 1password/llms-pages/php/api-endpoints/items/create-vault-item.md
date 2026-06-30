# Create Vault Item

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/php/x-redirect/JTI0ZSUyRkl0ZW1zJTJGQ3JlYXRlVmF1bHRJdGVt

```php
function createVaultItem(string $vaultUuid, ?FullItem $body = null): ApiResponse
```


# Authentication

This endpoint requires [ConnectToken](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/php/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `vaultUuid` | `string` | Template, Required | The UUID of the Vault to create an Item in<br><br>**Constraints**: *Pattern*: `^[\da-z]{26}$` |
| `body` | [`?FullItem`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/php/models/structures/full-item.md) | Body, Optional | - |


# Response Type

**200**: OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`FullItem`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/php/models/structures/full-item.md).


# Example Usage

```php
$vaultUuid = 'vaultUuid2';

$body = FullItemBuilder::init(
    Category::MEMBERSHIP,
    Vault1Builder::init(
        'id6'
    )->build()
)
    ->favorite(false)
    ->urls(
        [
            UrlBuilder::init(
                'https://example.com'
            )
                ->primary(true)
                ->build(),
            UrlBuilder::init(
                'https://example.org'
            )->build()
        ]
    )->build();

$itemsApi = $client->getItemsApi();
$apiResponse = $itemsApi->createVaultItem(
    $vaultUuid,
    $body
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'FullItem:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Unable to create item due to invalid input | [`ErrorResponseException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/php/models/exceptions/error-response.md) |
| 401 | Invalid or missing token | [`ErrorResponseException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/php/models/exceptions/error-response.md) |
| 403 | Unauthorized access | [`ErrorResponseException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/php/models/exceptions/error-response.md) |
| 404 | Item not found | [`ErrorResponseException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/php/models/exceptions/error-response.md) |



