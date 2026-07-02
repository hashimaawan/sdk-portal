# Rule 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlJ1bGUx

*This model accepts additional fields of type Object.*


# Class Name

`Rule1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ClusterUuid` | `String` | Optional | A unique ID for the database cluster to which the rule is applied.<br><br>**Constraints**: *Pattern*: `^$\|[0-9a-f]{8}\b-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{4}-\b[0-9a-f]{12}` | String getClusterUuid() | setClusterUuid(String clusterUuid) |
| `CreatedAt` | `LocalDateTime` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the firewall rule was created. | LocalDateTime getCreatedAt() | setCreatedAt(LocalDateTime createdAt) |
| `Type` | [`Type7`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/type-7.md) | Required | The type of resource that the firewall rule allows to access the database cluster. | Type7 getType() | setType(Type7 type) |
| `Uuid` | `String` | Optional | A unique ID for the firewall rule itself.<br><br>**Constraints**: *Pattern*: `^$\|[0-9a-f]{8}\b-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{4}-\b[0-9a-f]{12}` | String getUuid() | setUuid(String uuid) |
| `Value` | `String` | Required | The ID of the specific resource, the name of a tag applied to a group of resources, or the IP address that the firewall rule allows to access the database cluster. | String getValue() | setValue(String value) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.Rule1;
import com.digitalocean.api.models.Type7;
import java.io.IOException;

Rule1 rule1 = new Rule1.Builder(
    Type7.DROPLET,
    "ff2a6c52-5a44-4b63-b99c-0e98e7a63d61"
)
.clusterUuid("9cc10173-e9ea-4176-9dbc-a4cee4c4ff30")
.createdAt(DateTimeHelper.fromRfc8601DateTime("2019-01-11T18:37:36Z"))
.uuid("79f26d28-ea8a-41f2-8ad8-8cfcdd020095")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



