# Query Execution Statistics

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlF1ZXJ5RXhlY3V0aW9uU3RhdGlzdGljcw

The amount of data scanned during the query execution and the amount of time that it took to execute, and the type of statement that was run.


# Class Name

`QueryExecutionStatistics`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `engineExecutionTimeInMillis` | `?int` | Optional | - | getEngineExecutionTimeInMillis(): ?int | setEngineExecutionTimeInMillis(?int engineExecutionTimeInMillis): void |
| `dataScannedInBytes` | `?int` | Optional | - | getDataScannedInBytes(): ?int | setDataScannedInBytes(?int dataScannedInBytes): void |
| `dataManifestLocation` | `?string` | Optional | - | getDataManifestLocation(): ?string | setDataManifestLocation(?string dataManifestLocation): void |
| `totalExecutionTimeInMillis` | `?int` | Optional | - | getTotalExecutionTimeInMillis(): ?int | setTotalExecutionTimeInMillis(?int totalExecutionTimeInMillis): void |
| `queryQueueTimeInMillis` | `?int` | Optional | - | getQueryQueueTimeInMillis(): ?int | setQueryQueueTimeInMillis(?int queryQueueTimeInMillis): void |
| `queryPlanningTimeInMillis` | `?int` | Optional | - | getQueryPlanningTimeInMillis(): ?int | setQueryPlanningTimeInMillis(?int queryPlanningTimeInMillis): void |
| `serviceProcessingTimeInMillis` | `?int` | Optional | - | getServiceProcessingTimeInMillis(): ?int | setServiceProcessingTimeInMillis(?int serviceProcessingTimeInMillis): void |
| `resultReuseInformation` | [`?ResultReuseInformation2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/result-reuse-information-2.md) | Optional | - | getResultReuseInformation(): ?ResultReuseInformation2 | setResultReuseInformation(?ResultReuseInformation2 resultReuseInformation): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\QueryExecutionStatisticsBuilder;

$queryExecutionStatistics = QueryExecutionStatisticsBuilder::init()
    ->engineExecutionTimeInMillis(98)
    ->dataScannedInBytes(86)
    ->dataManifestLocation('DataManifestLocation2')
    ->totalExecutionTimeInMillis(136)
    ->queryQueueTimeInMillis(142)
    ->build();
```



