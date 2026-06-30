# Load Balancers Actions Delete Service Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwQWN0aW9ucyUyNTIwRGVsZXRlJTI1MjBTZXJ2aWNlJTI1MjBSZXF1ZXN0


# Class Name

`LoadBalancersActionsDeleteServiceRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `listenPort` | `float` | Required | The listen port of the service you want to delete | getListenPort(): float | setListenPort(float listenPort): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\LoadBalancersActionsDeleteServiceRequestBuilder;

$loadBalancersActionsDeleteServiceRequest = LoadBalancersActionsDeleteServiceRequestBuilder::init(
    4711
)->build();
```



