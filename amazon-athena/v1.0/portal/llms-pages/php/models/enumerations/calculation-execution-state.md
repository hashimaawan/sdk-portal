# Calculation Execution State

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkNhbGN1bGF0aW9uRXhlY3V0aW9uU3RhdGU


# Enum Type Name

`CalculationExecutionState`


# Fields

| Name |
|  --- |
| `CREATING` |
| `CREATED` |
| `QUEUED` |
| `RUNNING` |
| `CANCELING` |
| `CANCELED` |
| `COMPLETED` |
| `FAILED` |


# Example

```php
use AmazonAthenaLib\Models\CalculationExecutionState;

$calculationExecutionState = CalculationExecutionState::COMPLETED;
```



