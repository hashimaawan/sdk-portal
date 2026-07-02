# V2 Volumes Actions Request 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBWb2x1bWVzJTI1MjBBY3Rpb25zJTI1MjBSZXF1ZXN0Mg

*This model accepts additional fields of type Object.*


# Class Name

`V2VolumesActionsRequest2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Region` | [`Region2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/region-2.md) | Optional | The slug identifier for the region where the resource will initially be  available. | Region2 getRegion() | setRegion(Region2 region) |
| `Type` | [`Type21`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/type-21.md) | Required | The volume action to initiate. | Type21 getType() | setType(Type21 type) |
| `SizeGigabytes` | `int` | Required | The new size of the block storage volume in GiB (1024^3).<br><br>**Constraints**: `<= 16384` | int getSizeGigabytes() | setSizeGigabytes(int sizeGigabytes) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Region2;
import com.digitalocean.api.models.Type21;
import com.digitalocean.api.models.V2VolumesActionsRequest2;
import java.io.IOException;

V2VolumesActionsRequest2 v2VolumesActionsRequest2 = new V2VolumesActionsRequest2.Builder(
    Type21.ATTACH,
    15384
)
.region(Region2.NYC3)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



