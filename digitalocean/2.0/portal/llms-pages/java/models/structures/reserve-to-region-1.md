# Reserve to Region 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlJlc2VydmUlMjUyMHRvJTI1MjBSZWdpb24x

*This model accepts additional fields of type Object.*


# Class Name

`ReserveToRegion1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ProjectId` | `UUID` | Optional | The UUID of the project to which the reserved IP will be assigned. | UUID getProjectId() | setProjectId(UUID projectId) |
| `Region` | `String` | Required | The slug identifier for the region the reserved IP will be reserved to. | String getRegion() | setRegion(String region) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.ReserveToRegion1;
import java.io.IOException;
import java.util.UUID;

ReserveToRegion1 reserveToRegion1 = new ReserveToRegion1.Builder(
    "nyc3"
)
.projectId(UUID.fromString("746c6152-2fa2-11ed-92d3-27aaa54e4988"))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



