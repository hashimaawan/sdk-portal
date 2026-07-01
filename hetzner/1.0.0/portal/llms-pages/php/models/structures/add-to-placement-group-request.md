# Add to Placement Group Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkFkZFRvUGxhY2VtZW50R3JvdXBSZXF1ZXN0

*This model accepts additional fields of type array.*


# Class Name

`AddToPlacementGroupRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `placementGroup` | `int` | Required | ID of Placement Group the Server should be added to | getPlacementGroup(): int | setPlacementGroup(int placementGroup): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\AddToPlacementGroupRequestBuilder;
use HetznerCloudApiLib\ApiHelper;

$addToPlacementGroupRequest = AddToPlacementGroupRequestBuilder::init(
    1
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



