# Get Calculation Execution Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkdldENhbGN1bGF0aW9uRXhlY3V0aW9uUmVxdWVzdA


# Interface Name

`GetCalculationExecutionRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `calculationExecutionId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36` |


# Example

```ts
import { GetCalculationExecutionRequest } from 'amazon-athenalib';

const getCalculationExecutionRequest: GetCalculationExecutionRequest = {
  calculationExecutionId: 'CalculationExecutionId2',
};
```



