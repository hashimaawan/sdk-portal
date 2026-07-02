# Query Stage Plan

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlF1ZXJ5U3RhZ2VQbGFu


# Interface Name

`QueryStagePlan`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `string \| undefined` | Optional | - |
| `identifier` | `string \| undefined` | Optional | - |
| `children` | [`QueryStagePlanNode[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/query-stage-plan-node.md) | Optional | - |
| `remoteSources` | `string[] \| undefined` | Optional | - |


# Example

```ts
import { QueryStagePlan } from 'amazon-athenalib';

const queryStagePlan: QueryStagePlan = {
  name: 'Name0',
  identifier: 'Identifier6',
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
    }
  ],
  remoteSources: [
    'RemoteSources8',
    'RemoteSources9',
    'RemoteSources0'
  ],
};
```



