# Update Named Query Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlVwZGF0ZU5hbWVkUXVlcnlJbnB1dA

*This model accepts additional fields of type Object.*


# Class Name

`UpdateNamedQueryInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `NamedQueryId` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` | String getNamedQueryId() | setNamedQueryId(String namedQueryId) |
| `Name` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` | String getName() | setName(String name) |
| `Description` | `String` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `1024` | String getDescription() | setDescription(String description) |
| `QueryString` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `262144` | String getQueryString() | setQueryString(String queryString) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.UpdateNamedQueryInput;
import java.io.IOException;

UpdateNamedQueryInput updateNamedQueryInput = new UpdateNamedQueryInput.Builder(
    "NamedQueryId8",
    "Name4",
    "QueryString6"
)
.description("Description2")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



