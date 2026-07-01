# Change Protection Request 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkNoYW5nZVByb3RlY3Rpb25SZXF1ZXN0MQ

*This model accepts additional fields of type array.*


# Class Name

`ChangeProtectionRequest1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `delete` | `?bool` | Optional | If true, prevents the Network from being deleted | getDelete(): ?bool | setDelete(?bool delete): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\ChangeProtectionRequest1Builder;
use HetznerCloudApiLib\ApiHelper;

$changeProtectionRequest1 = ChangeProtectionRequest1Builder::init()
    ->delete(true)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



