# Output Stage

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRk91dHB1dFN0YWdl

*This model accepts additional fields of type unknown.*


# Interface Name

`OutputStage`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `stageId` | `number \| undefined` | Optional | - |
| `state` | `string \| undefined` | Optional | - |
| `outputBytes` | `number \| undefined` | Optional | - |
| `outputRows` | `number \| undefined` | Optional | - |
| `inputBytes` | `number \| undefined` | Optional | - |
| `inputRows` | `number \| undefined` | Optional | - |
| `executionTime` | `number \| undefined` | Optional | - |
| `queryStagePlan` | [`QueryStagePlan \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/query-stage-plan.md) | Optional | - |
| `subStages` | [`QueryStage[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/query-stage.md) | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { OutputStage } from 'amazon-athenalib';

const outputStage: OutputStage = {
  stageId: 26,
  state: 'State4',
  outputBytes: 212,
  outputRows: 54,
  inputBytes: 170,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



