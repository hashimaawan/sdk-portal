# Query Execution Statistics

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlF1ZXJ5RXhlY3V0aW9uU3RhdGlzdGljcw

The amount of data scanned during the query execution and the amount of time that it took to execute, and the type of statement that was run.


# Interface Name

`QueryExecutionStatistics`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `engineExecutionTimeInMillis` | `number \| undefined` | Optional | - |
| `dataScannedInBytes` | `number \| undefined` | Optional | - |
| `dataManifestLocation` | `string \| undefined` | Optional | - |
| `totalExecutionTimeInMillis` | `number \| undefined` | Optional | - |
| `queryQueueTimeInMillis` | `number \| undefined` | Optional | - |
| `queryPlanningTimeInMillis` | `number \| undefined` | Optional | - |
| `serviceProcessingTimeInMillis` | `number \| undefined` | Optional | - |
| `resultReuseInformation` | [`ResultReuseInformation2 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/result-reuse-information-2.md) | Optional | - |


# Example

```ts
import { QueryExecutionStatistics } from 'amazon-athenalib';

const queryExecutionStatistics: QueryExecutionStatistics = {
  engineExecutionTimeInMillis: 98,
  dataScannedInBytes: 86,
  dataManifestLocation: 'DataManifestLocation2',
  totalExecutionTimeInMillis: 136,
  queryQueueTimeInMillis: 142,
};
```



