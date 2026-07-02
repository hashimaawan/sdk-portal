# V2 Volumes Actions Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBWb2x1bWVzJTI1MjBBY3Rpb25zJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type Object.*


# Class Name

`V2VolumesActionsRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Region` | [`Region2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/region-2.md) | Optional | The slug identifier for the region where the resource will initially be  available. | Region2 getRegion() | setRegion(Region2 region) |
| `Type` | [`Type21`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/type-21.md) | Required | The volume action to initiate. | Type21 getType() | setType(Type21 type) |
| `DropletId` | `int` | Required | The unique identifier for the Droplet the volume will be attached or detached from. | int getDropletId() | setDropletId(int dropletId) |
| `Tags` | `List<String>` | Optional | A flat array of tag names as strings to be applied to the resource. Tag names may be for either existing or new tags. | List<String> getTags() | setTags(List<String> tags) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Region2;
import com.digitalocean.api.models.Type21;
import com.digitalocean.api.models.V2VolumesActionsRequest;
import java.io.IOException;
import java.util.Arrays;

V2VolumesActionsRequest v2VolumesActionsRequest = new V2VolumesActionsRequest.Builder(
    Type21.ATTACH,
    11612190
)
.region(Region2.NYC3)
.tags(Arrays.asList(
        "base-image",
        "prod"
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



