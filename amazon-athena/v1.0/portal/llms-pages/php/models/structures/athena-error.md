# Athena Error

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkF0aGVuYUVycm9y

Provides information about an Athena query error. The <code>AthenaError</code> feature provides standardized error information to help you understand failed queries and take steps after a query failure occurs. <code>AthenaError</code> includes an <code>ErrorCategory</code> field that specifies whether the cause of the failed query is due to system error, user error, or other error.


# Class Name

`AthenaError`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `errorCategory` | `?int` | Optional | **Constraints**: `>= 1`, `<= 3` | getErrorCategory(): ?int | setErrorCategory(?int errorCategory): void |
| `errorType` | `?int` | Optional | **Constraints**: `>= 0`, `<= 9999` | getErrorType(): ?int | setErrorType(?int errorType): void |
| `retryable` | `?bool` | Optional | - | getRetryable(): ?bool | setRetryable(?bool retryable): void |
| `errorMessage` | `?string` | Optional | - | getErrorMessage(): ?string | setErrorMessage(?string errorMessage): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\AthenaErrorBuilder;

$athenaError = AthenaErrorBuilder::init()
    ->errorCategory(3)
    ->errorType(238)
    ->retryable(false)
    ->errorMessage('ErrorMessage0')
    ->build();
```



