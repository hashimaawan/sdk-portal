# Get Query Runtime Statistics Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkdldFF1ZXJ5UnVudGltZVN0YXRpc3RpY3NPdXRwdXQ


# Interface Name

`GetQueryRuntimeStatisticsOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `queryRuntimeStatistics` | [`QueryRuntimeStatistics2 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/query-runtime-statistics-2.md) | Optional | - |


# Example

```ts
import { GetQueryRuntimeStatisticsOutput } from 'amazon-athenalib';

const getQueryRuntimeStatisticsOutput: GetQueryRuntimeStatisticsOutput = {
  queryRuntimeStatistics: {
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
  },
};
```



