# Patch Vault Item

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/php/x-redirect/JTI0ZSUyRkl0ZW1zJTJGUGF0Y2hWYXVsdEl0ZW0

Applies a modified [RFC6902 JSON Patch](https://tools.ietf.org/html/rfc6902) document to an Item or ItemField. This endpoint only supports `add`, `remove` and `replace` operations.

When modifying a specific ItemField, the ItemField's ID in the `path` attribute of the operation object: `/fields/{fieldId}`

```php
function patchVaultItem(string $vaultUuid, string $itemUuid, ?array $body = null): ApiResponse
```


# Authentication

This endpoint requires [ConnectToken](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/php/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `vaultUuid` | `string` | Template, Required | The UUID of the Vault the item is in<br><br>**Constraints**: *Pattern*: `^[\da-z]{26}$` |
| `itemUuid` | `string` | Template, Required | The UUID of the Item to update<br><br>**Constraints**: *Pattern*: `^[\da-z]{26}$` |
| `body` | [`?(Patch[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/php/models/structures/patch.md) | Body, Optional | - |


# Response Type

**200**: OK - Item updated. If no Patch operations were provided, Item is unmodified.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`FullItem`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/php/models/structures/full-item.md).


# Example Usage

```php
$vaultUuid = 'vaultUuid2';

$itemUuid = 'itemUuid6';

$body = [
    PatchBuilder::init(
        Op::ADD,
        '/fields'
    )
        ->value(ApiHelper::deserialize('{"label":"New Field","type":"string","value":"hunter2"}'))
        ->build()
];

$itemsApi = $client->getItemsApi();
$apiResponse = $itemsApi->patchVaultItem(
    $vaultUuid,
    $itemUuid,
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
| 401 | Invalid or missing token | [`ErrorResponseException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/php/models/exceptions/error-response.md) |
| 403 | Unauthorized access | [`ErrorResponseException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/php/models/exceptions/error-response.md) |
| 404 | Item not found | [`ErrorResponseException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/php/models/exceptions/error-response.md) |



