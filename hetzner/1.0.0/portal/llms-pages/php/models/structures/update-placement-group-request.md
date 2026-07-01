# Update Placement Group Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlVwZGF0ZVBsYWNlbWVudEdyb3VwUmVxdWVzdA


# Class Name

`UpdatePlacementGroupRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `labels` | `?array` | Optional | User-defined labels (key-value pairs) | getLabels(): ?array | setLabels(?array labels): void |
| `name` | `?string` | Optional | New PlacementGroup name | getName(): ?string | setName(?string name): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\UpdatePlacementGroupRequestBuilder;
use HetznerCloudAPILib\ApiHelper;

$updatePlacementGroupRequest = UpdatePlacementGroupRequestBuilder::init()
    ->labels(ApiHelper::deserialize('{"labelkey":"value"}'))
    ->name('my Placement Group')
    ->build();
```



