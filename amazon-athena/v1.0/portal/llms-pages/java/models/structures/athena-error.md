# Athena Error

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkF0aGVuYUVycm9y

Provides information about an Athena query error. The <code>AthenaError</code> feature provides standardized error information to help you understand failed queries and take steps after a query failure occurs. <code>AthenaError</code> includes an <code>ErrorCategory</code> field that specifies whether the cause of the failed query is due to system error, user error, or other error.


# Class Name

`AthenaError`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ErrorCategory` | `Integer` | Optional | **Constraints**: `>= 1`, `<= 3` | Integer getErrorCategory() | setErrorCategory(Integer errorCategory) |
| `ErrorType` | `Integer` | Optional | **Constraints**: `>= 0`, `<= 9999` | Integer getErrorType() | setErrorType(Integer errorType) |
| `Retryable` | `Boolean` | Optional | - | Boolean getRetryable() | setRetryable(Boolean retryable) |
| `ErrorMessage` | `String` | Optional | - | String getErrorMessage() | setErrorMessage(String errorMessage) |


# Example

```java
import com.amazonaws.useast1.athena.models.AthenaError;

AthenaError athenaError = new AthenaError.Builder()
    .errorCategory(3)
    .errorType(238)
    .retryable(false)
    .errorMessage("ErrorMessage0")
    .build();
```



