# Load Balancers Actions Change Algorithm Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwQWN0aW9ucyUyNTIwQ2hhbmdlJTI1MjBBbGdvcml0aG0lMjUyMFJlcXVlc3Q


# Class Name

`LoadBalancersActionsChangeAlgorithmRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `type` | [`string(Type39Enum)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/enumerations/type-39.md) | Required | Algorithm of the Load Balancer | getType(): string | setType(string type): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\LoadBalancersActionsChangeAlgorithmRequestBuilder;
use HetznerCloudAPILib\Models\Type39Enum;

$loadBalancersActionsChangeAlgorithmRequest = LoadBalancersActionsChangeAlgorithmRequestBuilder::init(
    Type39Enum::ROUND_ROBIN
)->build();
```



