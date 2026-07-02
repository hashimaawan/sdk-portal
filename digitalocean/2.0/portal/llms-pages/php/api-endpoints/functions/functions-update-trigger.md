# Functions Update Trigger

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0ZSUyRkZ1bmN0aW9ucyUyRmZ1bmN0aW9uc191cGRhdGVfdHJpZ2dlcg

Updates the details of the given trigger. To update a trigger, send a PUT request to `/v2/functions/namespaces/$NAMESPACE_ID/triggers/$TRIGGER_NAME` with new values for the `is_enabled ` or `scheduled_details` properties.

```php
function functionsUpdateTrigger(
    string $namespaceId,
    string $triggerName,
    V2FunctionsNamespacesTriggersRequest1 $body
): ApiResponse
```


# Authentication

This endpoint requires [bearer_auth](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `namespaceId` | `string` | Template, Required | The ID of the namespace to be managed. |
| `triggerName` | `string` | Template, Required | The name of the trigger to be managed. |
| `body` | [`V2FunctionsNamespacesTriggersRequest1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/v2-functions-namespaces-triggers-request-1.md) | Body, Required | - |


# Response Type

**200**: A JSON response object with a key called `trigger`. The object contains the properties associated
with the trigger.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`V2FunctionsNamespacesTriggersResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/v2-functions-namespaces-triggers-response-1.md).


# Example Usage

```php
$namespaceId = 'fn-xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx';

$triggerName = 'my trigger';

$body = V2FunctionsNamespacesTriggersRequest1Builder::init()
    ->isEnabled(true)
    ->build();

$functionsApi = $client->getFunctionsApi();
$apiResponse = $functionsApi->functionsUpdateTrigger(
    $namespaceId,
    $triggerName,
    $body
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'V2FunctionsNamespacesTriggersResponse1:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad Request. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |
| 401 | Unauthorized | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |
| 404 | Bad Request. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |
| 429 | API Rate limit exceeded | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |
| 500 | Server error. | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |
| Default | Unexpected error | [`V21Clicks401ErrorException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/exceptions/v2-1-clicks-401-error.md) |



