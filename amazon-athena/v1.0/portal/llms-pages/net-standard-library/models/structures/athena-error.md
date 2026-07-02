# Athena Error

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkF0aGVuYUVycm9y

Provides information about an Athena query error. The <code>AthenaError</code> feature provides standardized error information to help you understand failed queries and take steps after a query failure occurs. <code>AthenaError</code> includes an <code>ErrorCategory</code> field that specifies whether the cause of the failed query is due to system error, user error, or other error.


# Class Name

`AthenaError`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ErrorCategory` | `int?` | Optional | **Constraints**: `>= 1`, `<= 3` |
| `ErrorType` | `int?` | Optional | **Constraints**: `>= 0`, `<= 9999` |
| `Retryable` | `bool?` | Optional | - |
| `ErrorMessage` | `string` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;

AthenaError athenaError = new AthenaError
{
    ErrorCategory = 3,
    ErrorType = 238,
    Retryable = false,
    ErrorMessage = "ErrorMessage0",
};
```



