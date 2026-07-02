# Statistics

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlN0YXRpc3RpY3M

*This model accepts additional fields of type unknown.*


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
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { Statistics } from 'amazon-athenalib';

const statistics: Statistics = {
  engineExecutionTimeInMillis: 72,
  dataScannedInBytes: 60,
  dataManifestLocation: 'DataManifestLocation0',
  totalExecutionTimeInMillis: 146,
  queryQueueTimeInMillis: 116,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



