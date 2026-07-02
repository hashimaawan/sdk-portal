# Create Named Query Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkNyZWF0ZU5hbWVkUXVlcnlJbnB1dA

*This model accepts additional fields of type Object.*


# Class Name

`CreateNamedQueryInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Name` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` | String getName() | setName(String name) |
| `Description` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | String getDescription() | setDescription(String description) |
| `Database` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` | String getDatabase() | setDatabase(String database) |
| `QueryString` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `262144` | String getQueryString() | setQueryString(String queryString) |
| `ClientRequestToken` | `String` | Optional | **Constraints**: *Minimum Length*: `32`, *Maximum Length*: `128` | String getClientRequestToken() | setClientRequestToken(String clientRequestToken) |
| `WorkGroup` | `String` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` | String getWorkGroup() | setWorkGroup(String workGroup) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.CreateNamedQueryInput;
import java.io.IOException;

CreateNamedQueryInput createNamedQueryInput = new CreateNamedQueryInput.Builder(
    "Name4",
    "Database4",
    "QueryString8"
)
.description("Description0")
.clientRequestToken("ClientRequestToken0")
.workGroup("WorkGroup8")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



