# Get Calculation Execution Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkdldENhbGN1bGF0aW9uRXhlY3V0aW9uUmVzcG9uc2U


# Interface Name

`GetCalculationExecutionResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `calculationExecutionId` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36` |
| `sessionId` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `description` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `workingDirectory` | `string \| undefined` | Optional | **Constraints**: *Maximum Length*: `1024`, *Pattern*: `^(https\|s3\|S3)://([^/]+)/?(.*)$` |
| `status` | [`Status1 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/status-1.md) | Optional | - |
| `statistics` | [`Statistics1 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/statistics-1.md) | Optional | - |
| `result` | [`Result \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/result.md) | Optional | - |


# Example

```ts
import {
  CalculationExecutionState1Enum,
  GetCalculationExecutionResponse,
} from 'amazon-athenalib';

const getCalculationExecutionResponse: GetCalculationExecutionResponse = {
  calculationExecutionId: 'CalculationExecutionId4',
  sessionId: 'SessionId8',
  description: 'Description6',
  workingDirectory: 'WorkingDirectory8',
  status: {
    submissionDateTime: '2016-03-13T12:52:32.123Z',
    completionDateTime: '2016-03-13T12:52:32.123Z',
    state: CalculationExecutionState1Enum.CANCELING,
    stateChangeReason: 'StateChangeReason8',
  },
};
```



