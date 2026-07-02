# Start Calculation Execution Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlN0YXJ0Q2FsY3VsYXRpb25FeGVjdXRpb25SZXF1ZXN0

*This model accepts additional fields of type unknown.*


# Interface Name

`StartCalculationExecutionRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `sessionId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `description` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `calculationConfiguration` | [`GetCalculationExecutionCodeResponse \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/get-calculation-execution-code-response.md) | Optional | - |
| `codeBlock` | `string \| undefined` | Optional | **Constraints**: *Maximum Length*: `68000` |
| `clientRequestToken` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `32`, *Maximum Length*: `128` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { StartCalculationExecutionRequest } from 'amazon-athenalib';

const startCalculationExecutionRequest: StartCalculationExecutionRequest = {
  sessionId: 'SessionId4',
  description: 'Description2',
  calculationConfiguration: {
    codeBlock: 'CodeBlock4',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  codeBlock: 'CodeBlock6',
  clientRequestToken: 'ClientRequestToken8',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



