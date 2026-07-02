# Get Calculation Execution Code Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkdldENhbGN1bGF0aW9uRXhlY3V0aW9uQ29kZVJlcXVlc3Q

*This model accepts additional fields of type unknown.*


# Interface Name

`GetCalculationExecutionCodeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `calculationExecutionId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { GetCalculationExecutionCodeRequest } from 'amazon-athenalib';

const getCalculationExecutionCodeRequest: GetCalculationExecutionCodeRequest = {
  calculationExecutionId: 'CalculationExecutionId4',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



