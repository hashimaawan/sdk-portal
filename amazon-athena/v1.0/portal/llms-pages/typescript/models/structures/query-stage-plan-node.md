# Query Stage Plan Node

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlF1ZXJ5U3RhZ2VQbGFuTm9kZQ

Stage plan information such as name, identifier, sub plans, and remote sources.

*This model accepts additional fields of type unknown.*


# Interface Name

`QueryStagePlanNode`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `string \| undefined` | Optional | - |
| `identifier` | `string \| undefined` | Optional | - |
| `children` | [`QueryStagePlanNode[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/query-stage-plan-node.md) | Optional | - |
| `remoteSources` | `string[] \| undefined` | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { QueryStagePlanNode } from 'amazon-athenalib';

const queryStagePlanNode: QueryStagePlanNode = {
  name: 'Name4',
  identifier: 'Identifier0',
  children: [
    {
      name: 'Name6',
      identifier: 'Identifier2',
      children: [
        {
        }
      ],
      remoteSources: [
        'RemoteSources4',
        'RemoteSources5',
        'RemoteSources6'
      ],
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  remoteSources: [
    'RemoteSources2',
    'RemoteSources3',
    'RemoteSources4'
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



