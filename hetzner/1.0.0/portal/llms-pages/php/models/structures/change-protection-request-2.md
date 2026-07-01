# Change Protection Request 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkNoYW5nZVByb3RlY3Rpb25SZXF1ZXN0Mg


# Class Name

`ChangeProtectionRequest2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `delete` | `?bool` | Optional | If true, prevents the Primary IP from being deleted | getDelete(): ?bool | setDelete(?bool delete): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\ChangeProtectionRequest2Builder;

$changeProtectionRequest2 = ChangeProtectionRequest2Builder::init()
    ->delete(true)
    ->build();
```



