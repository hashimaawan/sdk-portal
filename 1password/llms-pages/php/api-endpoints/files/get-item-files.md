# Get Item Files

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/php/x-redirect/JTI0ZSUyRkZpbGVzJTJGR2V0SXRlbUZpbGVz

```php
function getItemFiles(string $vaultUuid, string $itemUuid, ?bool $inlineFiles = null): ApiResponse
```


# Authentication

This endpoint requires [ConnectToken](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/php/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `vaultUuid` | `string` | Template, Required | The UUID of the Vault to fetch Items from |
| `itemUuid` | `string` | Template, Required | The UUID of the Item to fetch files from |
| `inlineFiles` | `?bool` | Query, Optional | Tells server to return the base64-encoded file contents in the response. |


# Response Type

**200**: OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`File[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/php/models/structures/file.md).


# Example Usage

```php
$vaultUuid = '00002186-0000-0000-0000-000000000000';

$itemUuid = '0000141a-0000-0000-0000-000000000000';

$inlineFiles = true;

$filesApi = $client->getFilesApi();
$apiResponse = $filesApi->getItemFiles(
    $vaultUuid,
    $itemUuid,
    $inlineFiles
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'File[]:';
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
| 404 | Item not found | [`ErrorResponseException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/php/models/exceptions/error-response.md) |
| 413 | File content too large to display | [`ErrorResponseException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/php/models/exceptions/error-response.md) |



