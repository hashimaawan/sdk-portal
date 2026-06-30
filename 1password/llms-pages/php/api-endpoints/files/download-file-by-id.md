# Download File by ID

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/php/x-redirect/JTI0ZSUyRkZpbGVzJTJGRG93bmxvYWRGaWxlQnlJRA

```php
function downloadFileById(string $vaultUuid, string $itemUuid, string $fileUuid): ApiResponse
```


# Authentication

This endpoint requires [ConnectToken](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/php/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `vaultUuid` | `string` | Template, Required | The UUID of the Vault the item is in |
| `itemUuid` | `string` | Template, Required | The UUID of the Item the File is in |
| `fileUuid` | `string` | Template, Required | UUID of the file to get content from |


# Response Type

**200**: Success

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type `string`.


# Example Usage

```php
$vaultUuid = '00002186-0000-0000-0000-000000000000';

$itemUuid = '0000141a-0000-0000-0000-000000000000';

$fileUuid = 'fileUuid2';

$filesApi = $client->getFilesApi();
$apiResponse = $filesApi->downloadFileById(
    $vaultUuid,
    $itemUuid,
    $fileUuid
);

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


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Invalid or missing token | [`ErrorResponseException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/php/models/exceptions/error-response.md) |
| 404 | File not found | [`ErrorResponseException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/php/models/exceptions/error-response.md) |



