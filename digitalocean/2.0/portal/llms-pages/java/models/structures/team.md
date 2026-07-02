# Team

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlRlYW0

When authorized in a team context, includes information about the current team.

*This model accepts additional fields of type Object.*


# Class Name

`Team`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Name` | `String` | Optional | The name for the current team. | String getName() | setName(String name) |
| `Uuid` | `String` | Optional | The unique universal identifier for the current team. | String getUuid() | setUuid(String uuid) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Team;
import java.io.IOException;

Team team = new Team.Builder()
    .name("My Team")
    .uuid("5df3e3004a17e242b7c20ca6c9fc25b701a47ece")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



