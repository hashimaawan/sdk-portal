# Change Protection Request 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRkNoYW5nZVByb3RlY3Rpb25SZXF1ZXN0MQ


# Class Name

`ChangeProtectionRequest1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `delete` | `?bool` | Optional | If true, prevents the Network from being deleted | getDelete(): ?bool | setDelete(?bool delete): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\ChangeProtectionRequest1Builder;

$changeProtectionRequest1 = ChangeProtectionRequest1Builder::init()
    ->delete(true)
    ->build();
```



