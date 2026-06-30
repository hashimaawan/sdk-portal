# Add to Placement Group Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRkFkZFRvUGxhY2VtZW50R3JvdXBSZXF1ZXN0


# Class Name

`AddToPlacementGroupRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `PlacementGroup` | `int` | Required | ID of Placement Group the Server should be added to | int getPlacementGroup() | setPlacementGroup(int placementGroup) |


# Example

```java
import cloud.hetzner.api.models.AddToPlacementGroupRequest;

AddToPlacementGroupRequest addToPlacementGroupRequest = new AddToPlacementGroupRequest.Builder(
    1
)
.build();
```



