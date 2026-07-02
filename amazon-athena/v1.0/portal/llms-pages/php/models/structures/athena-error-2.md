# Athena Error 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkF0aGVuYUVycm9yMg

*This model accepts additional fields of type array.*


# Class Name

`AthenaError2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `errorCategory` | `?int` | Optional | **Constraints**: `>= 1`, `<= 3` | getErrorCategory(): ?int | setErrorCategory(?int errorCategory): void |
| `errorType` | `?int` | Optional | **Constraints**: `>= 0`, `<= 9999` | getErrorType(): ?int | setErrorType(?int errorType): void |
| `retryable` | `?bool` | Optional | - | getRetryable(): ?bool | setRetryable(?bool retryable): void |
| `errorMessage` | `?string` | Optional | - | getErrorMessage(): ?string | setErrorMessage(?string errorMessage): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\AthenaError2Builder;
use AmazonAthenaLib\ApiHelper;

$athenaError2 = AthenaError2Builder::init()
    ->errorCategory(3)
    ->errorType(56)
    ->retryable(false)
    ->errorMessage('ErrorMessage0')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



