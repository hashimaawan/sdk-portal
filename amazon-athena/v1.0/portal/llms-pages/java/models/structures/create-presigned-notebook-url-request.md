# Create Presigned Notebook Url Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkNyZWF0ZVByZXNpZ25lZE5vdGVib29rVXJsUmVxdWVzdA


# Class Name

`CreatePresignedNotebookUrlRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `SessionId` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | String getSessionId() | setSessionId(String sessionId) |


# Example

```java
import com.amazonaws.useast1.athena.models.CreatePresignedNotebookUrlRequest;

CreatePresignedNotebookUrlRequest createPresignedNotebookUrlRequest = new CreatePresignedNotebookUrlRequest.Builder(
    "SessionId0"
)
.build();
```



