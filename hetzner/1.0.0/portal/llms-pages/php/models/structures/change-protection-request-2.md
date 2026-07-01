# Change Protection Request 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkNoYW5nZVByb3RlY3Rpb25SZXF1ZXN0Mg

*This model accepts additional fields of type array.*


# Class Name

`ChangeProtectionRequest2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `delete` | `?bool` | Optional | If true, prevents the Primary IP from being deleted | getDelete(): ?bool | setDelete(?bool delete): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\ChangeProtectionRequest2Builder;
use HetznerCloudApiLib\ApiHelper;

$changeProtectionRequest2 = ChangeProtectionRequest2Builder::init()
    ->delete(true)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



