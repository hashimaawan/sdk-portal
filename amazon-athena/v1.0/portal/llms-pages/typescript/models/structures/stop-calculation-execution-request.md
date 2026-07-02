# Stop Calculation Execution Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlN0b3BDYWxjdWxhdGlvbkV4ZWN1dGlvblJlcXVlc3Q


# Interface Name

`StopCalculationExecutionRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `calculationExecutionId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36` |


# Example

```ts
import { StopCalculationExecutionRequest } from 'amazon-athenalib';

const stopCalculationExecutionRequest: StopCalculationExecutionRequest = {
  calculationExecutionId: 'CalculationExecutionId2',
};
```



