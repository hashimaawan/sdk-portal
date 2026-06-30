# Change Type Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRkNoYW5nZVR5cGVSZXF1ZXN0


# Class Name

`ChangeTypeRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `loadBalancerType` | `string` | Required | ID or name of Load Balancer type the Load Balancer should migrate to | getLoadBalancerType(): string | setLoadBalancerType(string loadBalancerType): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\ChangeTypeRequestBuilder;

$changeTypeRequest = ChangeTypeRequestBuilder::init(
    'lb21'
)->build();
```



