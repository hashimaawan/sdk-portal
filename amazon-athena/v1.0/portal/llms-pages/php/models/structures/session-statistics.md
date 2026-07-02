# Session Statistics

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlNlc3Npb25TdGF0aXN0aWNz

Contains statistics for a session.


# Class Name

`SessionStatistics`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `dpuExecutionInMillis` | `?int` | Optional | - | getDpuExecutionInMillis(): ?int | setDpuExecutionInMillis(?int dpuExecutionInMillis): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\SessionStatisticsBuilder;

$sessionStatistics = SessionStatisticsBuilder::init()
    ->dpuExecutionInMillis(188)
    ->build();
```



