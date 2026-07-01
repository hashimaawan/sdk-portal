# Get All Servers

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0ZSUyRlNlcnZlcnMlMkZHZXQlMjUyMGFsbCUyNTIwU2VydmVycw

Returns all existing Server objects

:information_source: **Note** This endpoint does not require authentication.

```php
function getAllServers(
    ?string $name = null,
    ?string $labelSelector = null,
    ?string $sort = null,
    ?string $status = null
): ApiResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `?string` | Query, Optional | Can be used to filter resources by their name. The response will only contain the resources matching the specified name |
| `labelSelector` | `?string` | Query, Optional | Can be used to filter resources by labels. The response will only contain resources matching the label selector. |
| `sort` | [`?string(Sort)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/enumerations/sort.md) | Query, Optional | Can be used multiple times. |
| `status` | [`?string(Status70)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/enumerations/status-70.md) | Query, Optional | Can be used multiple times. The response will only contain Server matching the status |


# Response Type

**200**: A paged array of servers

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`ServersResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/servers-response.md).


# Example Usage

```php
$serversApi = $client->getServersApi();
$apiResponse = $serversApi->getAllServers();

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'ServersResponse:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```



