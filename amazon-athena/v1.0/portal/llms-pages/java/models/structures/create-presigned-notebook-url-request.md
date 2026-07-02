# Create Presigned Notebook Url Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkNyZWF0ZVByZXNpZ25lZE5vdGVib29rVXJsUmVxdWVzdA

*This model accepts additional fields of type Object.*


# Class Name

`CreatePresignedNotebookUrlRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `SessionId` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | String getSessionId() | setSessionId(String sessionId) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.CreatePresignedNotebookUrlRequest;
import java.io.IOException;

CreatePresignedNotebookUrlRequest createPresignedNotebookUrlRequest = new CreatePresignedNotebookUrlRequest.Builder(
    "SessionId0"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



