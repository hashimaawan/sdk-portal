# Volumes Actions Resize Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlZvbHVtZXMlMjUyMEFjdGlvbnMlMjUyMFJlc2l6ZSUyNTIwUmVxdWVzdA

*This model accepts additional fields of type array.*


# Class Name

`VolumesActionsResizeRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `size` | `float` | Required | New Volume size in GB (must be greater than current size) | getSize(): float | setSize(float size): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\VolumesActionsResizeRequestBuilder;
use HetznerCloudApiLib\ApiHelper;

$volumesActionsResizeRequest = VolumesActionsResizeRequestBuilder::init(
    50
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



