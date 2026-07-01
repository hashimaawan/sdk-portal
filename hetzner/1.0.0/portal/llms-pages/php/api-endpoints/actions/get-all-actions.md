# Get All Actions

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0ZSUyRkFjdGlvbnMlMkZHZXQlMjUyMGFsbCUyNTIwQWN0aW9ucw

Returns all Action objects. You can `sort` the results by using the sort URI parameter, and filter them with the `status` parameter.

:information_source: **Note** This endpoint does not require authentication.

```php
function getAllActions(?int $id = null, ?string $sort = null, ?string $status = null): ApiResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `?int` | Query, Optional | Can be used multiple times, the response will contain only Actions with specified IDs |
| `sort` | [`?string(ParameterSort)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/enumerations/parameter-sort.md) | Query, Optional | Can be used multiple times. |
| `status` | [`?string(ParameterStatus)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/enumerations/parameter-status.md) | Query, Optional | Can be used multiple times, the response will contain only Actions with specified statuses |


# Response Type

**200**: The `actions` key contains a list of Actions

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`ActionsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/actions-response.md).


# Example Usage

```php
$actionsApi = $client->getActionsApi();
$apiResponse = $actionsApi->getAllActions();

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'ActionsResponse:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```



