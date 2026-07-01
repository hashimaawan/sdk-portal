# Add to Placement Group Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkFkZFRvUGxhY2VtZW50R3JvdXBSZXF1ZXN0

*This model accepts additional fields of type Object.*


# Class Name

`AddToPlacementGroupRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `PlacementGroup` | `int` | Required | ID of Placement Group the Server should be added to | int getPlacementGroup() | setPlacementGroup(int placementGroup) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.AddToPlacementGroupRequest;
import java.io.IOException;

AddToPlacementGroupRequest addToPlacementGroupRequest = new AddToPlacementGroupRequest.Builder(
    1
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



