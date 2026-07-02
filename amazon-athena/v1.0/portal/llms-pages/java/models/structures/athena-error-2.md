# Athena Error 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkF0aGVuYUVycm9yMg

*This model accepts additional fields of type Object.*


# Class Name

`AthenaError2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ErrorCategory` | `Integer` | Optional | **Constraints**: `>= 1`, `<= 3` | Integer getErrorCategory() | setErrorCategory(Integer errorCategory) |
| `ErrorType` | `Integer` | Optional | **Constraints**: `>= 0`, `<= 9999` | Integer getErrorType() | setErrorType(Integer errorType) |
| `Retryable` | `Boolean` | Optional | - | Boolean getRetryable() | setRetryable(Boolean retryable) |
| `ErrorMessage` | `String` | Optional | - | String getErrorMessage() | setErrorMessage(String errorMessage) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.AthenaError2;
import java.io.IOException;

AthenaError2 athenaError2 = new AthenaError2.Builder()
    .errorCategory(3)
    .errorType(56)
    .retryable(false)
    .errorMessage("ErrorMessage0")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



