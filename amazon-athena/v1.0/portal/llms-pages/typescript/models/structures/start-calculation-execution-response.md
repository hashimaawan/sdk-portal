# Start Calculation Execution Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlN0YXJ0Q2FsY3VsYXRpb25FeGVjdXRpb25SZXNwb25zZQ


# Interface Name

`StartCalculationExecutionResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `calculationExecutionId` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36` |
| `state` | [`CalculationExecutionState4Enum \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/enumerations/calculation-execution-state-4.md) | Optional | - |


# Example

```ts
import {
  CalculationExecutionState4Enum,
  StartCalculationExecutionResponse,
} from 'amazon-athenalib';

const startCalculationExecutionResponse: StartCalculationExecutionResponse = {
  calculationExecutionId: 'CalculationExecutionId0',
  state: CalculationExecutionState4Enum.CANCELING,
};
```



