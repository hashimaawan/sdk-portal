# Add to Placement Group Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRkFkZFRvUGxhY2VtZW50R3JvdXBSZXF1ZXN0


# Class Name

`AddToPlacementGroupRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `placementGroup` | `int` | Required | ID of Placement Group the Server should be added to | getPlacementGroup(): int | setPlacementGroup(int placementGroup): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\AddToPlacementGroupRequestBuilder;

$addToPlacementGroupRequest = AddToPlacementGroupRequestBuilder::init(
    1
)->build();
```



