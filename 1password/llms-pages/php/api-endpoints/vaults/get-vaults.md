# Get Vaults

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/php/x-redirect/JTI0ZSUyRlZhdWx0cyUyRkdldFZhdWx0cw

```php
function getVaults(?string $filter = null): ApiResponse
```


# Authentication

This endpoint requires [ConnectToken](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/php/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `filter` | `?string` | Query, Optional | Filter the Vault collection based on Vault name using SCIM eq filter |


# Response Type

**200**: OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`Vault[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/php/models/structures/vault.md).


# Example Usage

```php
$filter = 'name eq "Some Vault Name"';

$vaultsApi = $client->getVaultsApi();
$apiResponse = $vaultsApi->getVaults($filter);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'Vault[]:';
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



