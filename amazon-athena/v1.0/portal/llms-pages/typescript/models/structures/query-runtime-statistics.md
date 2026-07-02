# Query Runtime Statistics

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlF1ZXJ5UnVudGltZVN0YXRpc3RpY3M

The query execution timeline, statistics on input and output rows and bytes, and the different query stages that form the query execution plan.


# Interface Name

`QueryRuntimeStatistics`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `timeline` | [`QueryRuntimeStatisticsTimeline \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/query-runtime-statistics-timeline.md) | Optional | Timeline statistics such as query queue time, planning time, execution time, service processing time, and total execution time. |
| `rows` | [`QueryRuntimeStatisticsRows \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/query-runtime-statistics-rows.md) | Optional | Statistics such as input rows and bytes read by the query, rows and bytes output by the query, and the number of rows written by the query. |
| `outputStage` | [`OutputStage \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/output-stage.md) | Optional | - |


# Example

```ts
import { QueryRuntimeStatistics } from 'amazon-athenalib';

const queryRuntimeStatistics: QueryRuntimeStatistics = {
  timeline: {
    queryQueueTimeInMillis: 156,
    queryPlanningTimeInMillis: 82,
    engineExecutionTimeInMillis: 112,
    serviceProcessingTimeInMillis: 126,
    totalExecutionTimeInMillis: 106,
  },
  rows: {
    inputRows: 230,
    inputBytes: 250,
    outputBytes: 36,
    outputRows: 230,
  },
  outputStage: {
    stageId: 130,
    state: 'State0',
    outputBytes: 108,
    outputRows: 158,
    inputBytes: 190,
  },
};
```



