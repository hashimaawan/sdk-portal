# Volumes Actions Change Protection Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlZvbHVtZXMlMjUyMEFjdGlvbnMlMjUyMENoYW5nZSUyNTIwUHJvdGVjdGlvbiUyNTIwUmVxdWVzdA

*This model accepts additional fields of type array.*


# Class Name

`VolumesActionsChangeProtectionRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `delete` | `?bool` | Optional | If true, prevents the Volume from being deleted | getDelete(): ?bool | setDelete(?bool delete): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\VolumesActionsChangeProtectionRequestBuilder;
use HetznerCloudApiLib\ApiHelper;

$volumesActionsChangeProtectionRequest = VolumesActionsChangeProtectionRequestBuilder::init()
    ->delete(true)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



