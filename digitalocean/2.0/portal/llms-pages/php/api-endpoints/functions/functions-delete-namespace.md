# Functions Delete Namespace

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0ZSUyRkZ1bmN0aW9ucyUyRmZ1bmN0aW9uc19kZWxldGVfbmFtZXNwYWNl

Deletes the given namespace.  When a namespace is deleted all assets, in the namespace are deleted, this includes packages, functions and triggers. Deleting a namespace is a destructive operation and assets in the namespace are not recoverable after deletion. Some metadata is retained, such as activations, or soft deleted for reporting purposes.
To delete namespace, send a DELETE request to `/v2/functions/namespaces/$NAMESPACE_ID`.
A successful deletion returns a 204 response.

```php
function functionsDeleteNamespace(string $namespaceId): ApiResponse
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `namespaceId` | `string` | Template, Required | The ID of the namespace to be managed. |


# Response Type

**204**: The action was successful and the response body is empty.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```php
$namespaceId = 'fn-xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx';

$functionsApi = $client->getFunctionsApi();
$apiResponse = $functionsApi->functionsDeleteNamespace($namespaceId);

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


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |
| 404 | Bad Request. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |



