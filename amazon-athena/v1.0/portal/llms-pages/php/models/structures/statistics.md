# Statistics

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlN0YXRpc3RpY3M


# Class Name

`Statistics`


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
use AmazonAthenaLib\Models\Builders\StatisticsBuilder;

$statistics = StatisticsBuilder::init()
    ->engineExecutionTimeInMillis(72)
    ->dataScannedInBytes(60)
    ->dataManifestLocation('DataManifestLocation0')
    ->totalExecutionTimeInMillis(146)
    ->queryQueueTimeInMillis(116)
    ->build();
```



