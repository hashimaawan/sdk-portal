# Create Notebook Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkNyZWF0ZU5vdGVib29rSW5wdXQ

*This model accepts additional fields of type Object.*


# Class Name

`CreateNotebookInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `WorkGroup` | `String` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` | String getWorkGroup() | setWorkGroup(String workGroup) |
| `Name` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` | String getName() | setName(String name) |
| `ClientRequestToken` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36`, *Pattern*: `[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}` | String getClientRequestToken() | setClientRequestToken(String clientRequestToken) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.CreateNotebookInput;
import java.io.IOException;

CreateNotebookInput createNotebookInput = new CreateNotebookInput.Builder(
    "WorkGroup2",
    "Name0"
)
.clientRequestToken("ClientRequestToken4")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



