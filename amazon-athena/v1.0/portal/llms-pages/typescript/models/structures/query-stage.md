# Query Stage

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlF1ZXJ5U3RhZ2U

Stage statistics such as input and output rows and bytes, execution time and stage state. This information also includes substages and the query stage plan.

*This model accepts additional fields of type unknown.*


# Interface Name

`QueryStage`


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
import { QueryStage } from 'amazon-athenalib';

const queryStage: QueryStage = {
  stageId: 118,
  state: 'State0',
  outputBytes: 120,
  outputRows: 146,
  inputBytes: 178,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



