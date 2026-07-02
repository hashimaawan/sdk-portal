# Query Runtime Statistics Timeline

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlF1ZXJ5UnVudGltZVN0YXRpc3RpY3NUaW1lbGluZQ

Timeline statistics such as query queue time, planning time, execution time, service processing time, and total execution time.


# Interface Name

`QueryRuntimeStatisticsTimeline`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `queryQueueTimeInMillis` | `number \| undefined` | Optional | - |
| `queryPlanningTimeInMillis` | `number \| undefined` | Optional | - |
| `engineExecutionTimeInMillis` | `number \| undefined` | Optional | - |
| `serviceProcessingTimeInMillis` | `number \| undefined` | Optional | - |
| `totalExecutionTimeInMillis` | `number \| undefined` | Optional | - |


# Example

```ts
import { QueryRuntimeStatisticsTimeline } from 'amazon-athenalib';

const queryRuntimeStatisticsTimeline: QueryRuntimeStatisticsTimeline = {
  queryQueueTimeInMillis: 122,
  queryPlanningTimeInMillis: 48,
  engineExecutionTimeInMillis: 78,
  serviceProcessingTimeInMillis: 96,
  totalExecutionTimeInMillis: 140,
};
```



