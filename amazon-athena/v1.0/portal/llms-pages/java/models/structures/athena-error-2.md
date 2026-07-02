# Athena Error 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkF0aGVuYUVycm9yMg


# Class Name

`AthenaError2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ErrorCategory` | `Integer` | Optional | **Constraints**: `>= 1`, `<= 3` | Integer getErrorCategory() | setErrorCategory(Integer errorCategory) |
| `ErrorType` | `Integer` | Optional | **Constraints**: `>= 0`, `<= 9999` | Integer getErrorType() | setErrorType(Integer errorType) |
| `Retryable` | `Boolean` | Optional | - | Boolean getRetryable() | setRetryable(Boolean retryable) |
| `ErrorMessage` | `String` | Optional | - | String getErrorMessage() | setErrorMessage(String errorMessage) |


# Example

```java
import com.amazonaws.useast1.athena.models.AthenaError2;

AthenaError2 athenaError2 = new AthenaError2.Builder()
    .errorCategory(3)
    .errorType(56)
    .retryable(false)
    .errorMessage("ErrorMessage0")
    .build();
```



