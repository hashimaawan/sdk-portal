# Get Calculation Execution Code Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkdldENhbGN1bGF0aW9uRXhlY3V0aW9uQ29kZVJlcXVlc3Q


# Interface Name

`GetCalculationExecutionCodeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `calculationExecutionId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36` |


# Example

```ts
import { GetCalculationExecutionCodeRequest } from 'amazon-athenalib';

const getCalculationExecutionCodeRequest: GetCalculationExecutionCodeRequest = {
  calculationExecutionId: 'CalculationExecutionId4',
};
```



