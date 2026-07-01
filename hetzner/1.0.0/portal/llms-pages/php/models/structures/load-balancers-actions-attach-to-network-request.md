# Load Balancers Actions Attach to Network Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwQWN0aW9ucyUyNTIwQXR0YWNoJTI1MjBUbyUyNTIwTmV0d29yayUyNTIwUmVxdWVzdA

*This model accepts additional fields of type array.*


# Class Name

`LoadBalancersActionsAttachToNetworkRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ip` | `?string` | Optional | IP to request to be assigned to this Load Balancer; if you do not provide this then you will be auto assigned an IP address | getIp(): ?string | setIp(?string ip): void |
| `network` | `float` | Required | ID of an existing network to attach the Load Balancer to | getNetwork(): float | setNetwork(float network): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\LoadBalancersActionsAttachToNetworkRequestBuilder;
use HetznerCloudApiLib\ApiHelper;

$loadBalancersActionsAttachToNetworkRequest = LoadBalancersActionsAttachToNetworkRequestBuilder::init(
    4711
)
    ->ip('10.0.1.1')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



