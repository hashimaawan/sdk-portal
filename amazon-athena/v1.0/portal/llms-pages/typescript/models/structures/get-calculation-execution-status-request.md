# Get Calculation Execution Status Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkdldENhbGN1bGF0aW9uRXhlY3V0aW9uU3RhdHVzUmVxdWVzdA

*This model accepts additional fields of type unknown.*


# Interface Name

`GetCalculationExecutionStatusRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `calculationExecutionId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { GetCalculationExecutionStatusRequest } from 'amazon-athenalib';

const getCalculationExecutionStatusRequest: GetCalculationExecutionStatusRequest = {
  calculationExecutionId: 'CalculationExecutionId8',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



