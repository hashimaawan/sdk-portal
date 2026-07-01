# Get All Networks

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0ZSUyRk5ldHdvcmtzJTJGR2V0JTI1MjBhbGwlMjUyME5ldHdvcmtz

Gets all existing networks that you have available.

:information_source: **Note** This endpoint does not require authentication.

```php
function getAllNetworks(?string $name = null, ?string $labelSelector = null): NetworksResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `?string` | Query, Optional | Can be used to filter networks by their name. The response will only contain the networks matching the specified name. |
| `labelSelector` | `?string` | Query, Optional | Can be used to filter networks by labels. The response will only contain networks with a matching label selector pattern. |


# Response Type

**200**: The `networks` key contains a list of networks

[`NetworksResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/networks-response.md)


# Example Usage

```php
$networksController = $client->getNetworksController();

try {
    $result = $networksController->getAllNetworks();
    echo 'NetworksResponse:';
    var_dump($result);
} catch (ApiException $exp) {
    echo 'Caught:', $exp;
}
```



