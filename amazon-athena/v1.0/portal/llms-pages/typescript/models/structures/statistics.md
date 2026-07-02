# Statistics

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlN0YXRpc3RpY3M


# Interface Name

`Statistics`


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
import { Statistics } from 'amazon-athenalib';

const statistics: Statistics = {
  engineExecutionTimeInMillis: 72,
  dataScannedInBytes: 60,
  dataManifestLocation: 'DataManifestLocation0',
  totalExecutionTimeInMillis: 146,
  queryQueueTimeInMillis: 116,
};
```



