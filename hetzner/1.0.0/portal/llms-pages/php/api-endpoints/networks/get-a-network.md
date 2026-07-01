# Get a Network

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0ZSUyRk5ldHdvcmtzJTJGR2V0JTI1MjBhJTI1MjBOZXR3b3Jr

Gets a specific network object.

:information_source: **Note** This endpoint does not require authentication.

```php
function getANetwork(int $id): NetworksResponse1
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the network |


# Response Type

**200**: The `network` key contains the network

[`NetworksResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/networks-response-1.md)


# Example Usage

```php
$id = 112;

$networksController = $client->getNetworksController();

try {
    $result = $networksController->getANetwork($id);
    echo 'NetworksResponse1:';
    var_dump($result);
} catch (ApiException $exp) {
    echo 'Caught:', $exp;
}
```



