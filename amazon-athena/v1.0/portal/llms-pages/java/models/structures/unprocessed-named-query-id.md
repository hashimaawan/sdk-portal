# Unprocessed Named Query Id

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlVucHJvY2Vzc2VkTmFtZWRRdWVyeUlk

Information about a named query ID that could not be processed.

*This model accepts additional fields of type Object.*


# Class Name

`UnprocessedNamedQueryId`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `NamedQueryId` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` | String getNamedQueryId() | setNamedQueryId(String namedQueryId) |
| `ErrorCode` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | String getErrorCode() | setErrorCode(String errorCode) |
| `ErrorMessage` | `String` | Optional | - | String getErrorMessage() | setErrorMessage(String errorMessage) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.UnprocessedNamedQueryId;
import java.io.IOException;

UnprocessedNamedQueryId unprocessedNamedQueryId = new UnprocessedNamedQueryId.Builder()
    .namedQueryId("NamedQueryId0")
    .errorCode("ErrorCode8")
    .errorMessage("ErrorMessage8")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



