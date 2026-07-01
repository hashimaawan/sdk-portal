# Load Balancers Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwUmVxdWVzdA


# Class Name

`LoadBalancersRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `labels` | `?array` | Optional | User-defined labels (key-value pairs) | getLabels(): ?array | setLabels(?array labels): void |
| `name` | `?string` | Optional | New Load Balancer name | getName(): ?string | setName(?string name): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\LoadBalancersRequestBuilder;
use HetznerCloudAPILib\ApiHelper;

$loadBalancersRequest = LoadBalancersRequestBuilder::init()
    ->labels(ApiHelper::deserialize('{"labelkey":"value"}'))
    ->name('new-name')
    ->build();
```



