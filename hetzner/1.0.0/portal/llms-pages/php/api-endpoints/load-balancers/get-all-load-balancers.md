# Get All Load Balancers

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0ZSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyRkdldCUyNTIwYWxsJTI1MjBMb2FkJTI1MjBCYWxhbmNlcnM

Gets all existing Load Balancers that you have available.

:information_source: **Note** This endpoint does not require authentication.

```php
function getAllLoadBalancers(
    ?string $sort = null,
    ?string $name = null,
    ?string $labelSelector = null
): LoadBalancersResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `sort` | [`?string(SortEnum)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/enumerations/sort.md) | Query, Optional | Can be used multiple times. |
| `name` | `?string` | Query, Optional | Can be used to filter resources by their name. The response will only contain the resources matching the specified name |
| `labelSelector` | `?string` | Query, Optional | Can be used to filter resources by labels. The response will only contain resources matching the label selector. |


# Response Type

**200**: The `load_balancers` key contains a list of Load Balancers

[`LoadBalancersResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/load-balancers-response.md)


# Example Usage

```php
$loadBalancersController = $client->getLoadBalancersController();

try {
    $result = $loadBalancersController->getAllLoadBalancers();
    echo 'LoadBalancersResponse:';
    var_dump($result);
} catch (ApiException $exp) {
    echo 'Caught:', $exp;
}
```



