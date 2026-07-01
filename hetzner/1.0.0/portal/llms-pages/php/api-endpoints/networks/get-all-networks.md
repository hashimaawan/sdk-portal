# Get All Networks

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0ZSUyRk5ldHdvcmtzJTJGR2V0JTI1MjBhbGwlMjUyME5ldHdvcmtz

Gets all existing networks that you have available.

:information_source: **Note** This endpoint does not require authentication.

```php
function getAllNetworks(?string $name = null, ?string $labelSelector = null): ApiResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `?string` | Query, Optional | Can be used to filter networks by their name. The response will only contain the networks matching the specified name. |
| `labelSelector` | `?string` | Query, Optional | Can be used to filter networks by labels. The response will only contain networks with a matching label selector pattern. |


# Response Type

**200**: The `networks` key contains a list of networks

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`NetworksResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/networks-response.md).


# Example Usage

```php
$networksApi = $client->getNetworksApi();
$apiResponse = $networksApi->getAllNetworks();

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'NetworksResponse:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
}
```



