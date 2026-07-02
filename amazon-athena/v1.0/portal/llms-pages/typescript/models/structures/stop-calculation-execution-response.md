# Stop Calculation Execution Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlN0b3BDYWxjdWxhdGlvbkV4ZWN1dGlvblJlc3BvbnNl


# Interface Name

`StopCalculationExecutionResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `state` | [`CalculationExecutionState4Enum \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/enumerations/calculation-execution-state-4.md) | Optional | - |


# Example

```ts
import {
  CalculationExecutionState4Enum,
  StopCalculationExecutionResponse,
} from 'amazon-athenalib';

const stopCalculationExecutionResponse: StopCalculationExecutionResponse = {
  state: CalculationExecutionState4Enum.QUEUED,
};
```



