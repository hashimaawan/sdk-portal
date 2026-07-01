# Update Placement Group Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlVwZGF0ZVBsYWNlbWVudEdyb3VwUmVxdWVzdA

*This model accepts additional fields of type array.*


# Class Name

`UpdatePlacementGroupRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `labels` | `?array` | Optional | User-defined labels (key-value pairs) | getLabels(): ?array | setLabels(?array labels): void |
| `name` | `?string` | Optional | New PlacementGroup name | getName(): ?string | setName(?string name): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\UpdatePlacementGroupRequestBuilder;
use HetznerCloudApiLib\ApiHelper;

$updatePlacementGroupRequest = UpdatePlacementGroupRequestBuilder::init()
    ->labels(ApiHelper::deserialize('{"labelkey":"value"}'))
    ->name('my Placement Group')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



