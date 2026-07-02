# Action 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkFjdGlvbjI

*This model accepts additional fields of type Object.*


# Class Name

`Action2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CompletedAt` | `LocalDateTime` | Optional | A time value given in ISO8601 combined date and time format that represents when the action was completed. | LocalDateTime getCompletedAt() | setCompletedAt(LocalDateTime completedAt) |
| `Id` | `Integer` | Optional | A unique numeric ID that can be used to identify and reference an action. | Integer getId() | setId(Integer id) |
| `Region` | [`Region`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/region.md) | Optional | - | Region getRegion() | setRegion(Region region) |
| `RegionSlug` | `String` | Optional | - | String getRegionSlug() | setRegionSlug(String regionSlug) |
| `ResourceId` | `Integer` | Optional | A unique identifier for the resource that the action is associated with. | Integer getResourceId() | setResourceId(Integer resourceId) |
| `ResourceType` | `String` | Optional | The type of resource that the action is associated with. | String getResourceType() | setResourceType(String resourceType) |
| `StartedAt` | `LocalDateTime` | Optional | A time value given in ISO8601 combined date and time format that represents when the action was initiated. | LocalDateTime getStartedAt() | setStartedAt(LocalDateTime startedAt) |
| `Status` | [`Status1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/status-1.md) | Optional | The current status of the action. This can be "in-progress", "completed", or "errored".<br><br>**Default**: `Status1.INPROGRESS` | Status1 getStatus() | setStatus(Status1 status) |
| `Type` | `String` | Optional | This is the type of action that the object represents. For example, this could be "transfer" to represent the state of an image transfer action. | String getType() | setType(String type) |
| `ProjectId` | `UUID` | Optional | The UUID of the project to which the reserved IP currently belongs. | UUID getProjectId() | setProjectId(UUID projectId) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.Action2;
import com.digitalocean.api.models.Region;
import com.digitalocean.api.models.Status1;
import java.io.IOException;
import java.util.Arrays;
import java.util.UUID;

Action2 action2 = new Action2.Builder()
    .completedAt(DateTimeHelper.fromRfc8601DateTime("2020-11-14T16:30:06Z"))
    .id(36804636)
    .region(new Region.Builder(
        false,
        Arrays.asList(
            "features7",
            "features8",
            "features9"
        ),
        "name6",
        Arrays.asList(
            "sizes6"
        ),
        "slug0"
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build())
    .regionSlug("region_slug8")
    .resourceId(3164444)
    .resourceType("droplet")
    .startedAt(DateTimeHelper.fromRfc8601DateTime("2020-11-14T16:29:21Z"))
    .status(Status1.COMPLETED)
    .type("create")
    .projectId(UUID.fromString("746c6152-2fa2-11ed-92d3-27aaa54e4988"))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



