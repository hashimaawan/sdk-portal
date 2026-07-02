# Stop Calculation Execution Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlN0b3BDYWxjdWxhdGlvbkV4ZWN1dGlvblJlc3BvbnNl

*This model accepts additional fields of type unknown.*


# Interface Name

`StopCalculationExecutionResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `state` | [`CalculationExecutionState4 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/enumerations/calculation-execution-state-4.md) | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  CalculationExecutionState4,
  StopCalculationExecutionResponse,
} from 'amazon-athenalib';

const stopCalculationExecutionResponse: StopCalculationExecutionResponse = {
  state: CalculationExecutionState4.Queued,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



