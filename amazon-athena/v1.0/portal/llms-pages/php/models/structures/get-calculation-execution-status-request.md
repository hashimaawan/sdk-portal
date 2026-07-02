# Get Calculation Execution Status Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkdldENhbGN1bGF0aW9uRXhlY3V0aW9uU3RhdHVzUmVxdWVzdA


# Class Name

`GetCalculationExecutionStatusRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `calculationExecutionId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36` | getCalculationExecutionId(): string | setCalculationExecutionId(string calculationExecutionId): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\GetCalculationExecutionStatusRequestBuilder;

$getCalculationExecutionStatusRequest = GetCalculationExecutionStatusRequestBuilder::init(
    'CalculationExecutionId8'
)->build();
```



