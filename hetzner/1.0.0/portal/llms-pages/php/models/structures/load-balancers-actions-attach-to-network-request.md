# Load Balancers Actions Attach to Network Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwQWN0aW9ucyUyNTIwQXR0YWNoJTI1MjBUbyUyNTIwTmV0d29yayUyNTIwUmVxdWVzdA


# Class Name

`LoadBalancersActionsAttachToNetworkRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ip` | `?string` | Optional | IP to request to be assigned to this Load Balancer; if you do not provide this then you will be auto assigned an IP address | getIp(): ?string | setIp(?string ip): void |
| `network` | `float` | Required | ID of an existing network to attach the Load Balancer to | getNetwork(): float | setNetwork(float network): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\LoadBalancersActionsAttachToNetworkRequestBuilder;

$loadBalancersActionsAttachToNetworkRequest = LoadBalancersActionsAttachToNetworkRequestBuilder::init(
    4711
)
    ->ip('10.0.1.1')
    ->build();
```



