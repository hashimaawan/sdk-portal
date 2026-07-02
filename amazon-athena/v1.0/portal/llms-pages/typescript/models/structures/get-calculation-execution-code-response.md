# Get Calculation Execution Code Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkdldENhbGN1bGF0aW9uRXhlY3V0aW9uQ29kZVJlc3BvbnNl

*This model accepts additional fields of type unknown.*


# Interface Name

`GetCalculationExecutionCodeResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `codeBlock` | `string \| undefined` | Optional | **Constraints**: *Maximum Length*: `68000` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { GetCalculationExecutionCodeResponse } from 'amazon-athenalib';

const getCalculationExecutionCodeResponse: GetCalculationExecutionCodeResponse = {
  codeBlock: 'CodeBlock4',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



