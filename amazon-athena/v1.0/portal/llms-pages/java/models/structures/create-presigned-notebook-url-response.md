# Create Presigned Notebook Url Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkNyZWF0ZVByZXNpZ25lZE5vdGVib29rVXJsUmVzcG9uc2U


# Class Name

`CreatePresignedNotebookUrlResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `NotebookUrl` | `String` | Required | - | String getNotebookUrl() | setNotebookUrl(String notebookUrl) |
| `AuthToken` | `String` | Required | **Constraints**: *Maximum Length*: `2048` | String getAuthToken() | setAuthToken(String authToken) |
| `AuthTokenExpirationTime` | `int` | Required | - | int getAuthTokenExpirationTime() | setAuthTokenExpirationTime(int authTokenExpirationTime) |


# Example

```java
import com.amazonaws.useast1.athena.models.CreatePresignedNotebookUrlResponse;

CreatePresignedNotebookUrlResponse createPresignedNotebookUrlResponse = new CreatePresignedNotebookUrlResponse.Builder(
    "NotebookUrl0",
    "AuthToken4",
    240
)
.build();
```



