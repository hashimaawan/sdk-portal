# Create Placement Group Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkNyZWF0ZVBsYWNlbWVudEdyb3VwUmVxdWVzdA


# Class Name

`CreatePlacementGroupRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `labels` | `?array` | Optional | User-defined labels (key-value pairs) | getLabels(): ?array | setLabels(?array labels): void |
| `name` | `string` | Required | Name of the PlacementGroup | getName(): string | setName(string name): void |
| `type` | `string` | Required, Constant | Define the Placement Group Type.<br><br>**Value**: `'spread'` | getType(): string | setType(string type): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\CreatePlacementGroupRequestBuilder;
use HetznerCloudAPILib\ApiHelper;

$createPlacementGroupRequest = CreatePlacementGroupRequestBuilder::init(
    'my Placement Group'
)
    ->labels(ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



