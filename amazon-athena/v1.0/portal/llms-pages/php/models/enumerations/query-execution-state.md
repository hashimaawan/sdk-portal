# Query Execution State

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlF1ZXJ5RXhlY3V0aW9uU3RhdGU


# Enum Type Name

`QueryExecutionState`


# Fields

| Name |
|  --- |
| `QUEUED` |
| `RUNNING` |
| `SUCCEEDED` |
| `FAILED` |
| `CANCELLED` |


# Example

```php
use AmazonAthenaLib\Models\QueryExecutionState;

$queryExecutionState = QueryExecutionState::CANCELLED;
```



