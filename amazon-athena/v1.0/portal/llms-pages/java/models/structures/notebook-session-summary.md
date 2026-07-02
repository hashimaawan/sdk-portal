# Notebook Session Summary

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRk5vdGVib29rU2Vzc2lvblN1bW1hcnk

Contains the notebook session ID and notebook session creation time.

*This model accepts additional fields of type Object.*


# Class Name

`NotebookSessionSummary`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `SessionId` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | String getSessionId() | setSessionId(String sessionId) |
| `CreationTime` | `LocalDateTime` | Optional | - | LocalDateTime getCreationTime() | setCreationTime(LocalDateTime creationTime) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.DateTimeHelper;
import com.amazonaws.useast1.athena.models.NotebookSessionSummary;
import java.io.IOException;

NotebookSessionSummary notebookSessionSummary = new NotebookSessionSummary.Builder()
    .sessionId("SessionId0")
    .creationTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



