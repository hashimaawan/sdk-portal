# Named Query 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRk5hbWVkUXVlcnkx

*This model accepts additional fields of type Object.*


# Class Name

`NamedQuery1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Name` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` | String getName() | setName(String name) |
| `Description` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | String getDescription() | setDescription(String description) |
| `Database` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` | String getDatabase() | setDatabase(String database) |
| `QueryString` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `262144` | String getQueryString() | setQueryString(String queryString) |
| `NamedQueryId` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` | String getNamedQueryId() | setNamedQueryId(String namedQueryId) |
| `WorkGroup` | `String` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` | String getWorkGroup() | setWorkGroup(String workGroup) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.NamedQuery1;
import java.io.IOException;

NamedQuery1 namedQuery1 = new NamedQuery1.Builder(
    "Name0",
    "Database8",
    "QueryString2"
)
.description("Description6")
.namedQueryId("NamedQueryId2")
.workGroup("WorkGroup2")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



