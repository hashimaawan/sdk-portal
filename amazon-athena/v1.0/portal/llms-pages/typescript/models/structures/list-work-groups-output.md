# List Work Groups Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkxpc3RXb3JrR3JvdXBzT3V0cHV0


# Interface Name

`ListWorkGroupsOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `workGroups` | [`WorkGroupSummary[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/work-group-summary.md) | Optional | **Constraints**: *Minimum Items*: `0`, *Maximum Items*: `50` |
| `nextToken` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |


# Example

```ts
import { ListWorkGroupsOutput, WorkGroupState1Enum } from 'amazon-athenalib';

const listWorkGroupsOutput: ListWorkGroupsOutput = {
  workGroups: [
    {
      name: 'Name4',
      state: WorkGroupState1Enum.ENABLED,
      description: 'Description0',
      creationTime: '2016-03-13T12:52:32.123Z',
      engineVersion: {
        selectedEngineVersion: 'SelectedEngineVersion4',
        effectiveEngineVersion: 'EffectiveEngineVersion6',
      },
    },
    {
      name: 'Name4',
      state: WorkGroupState1Enum.ENABLED,
      description: 'Description0',
      creationTime: '2016-03-13T12:52:32.123Z',
      engineVersion: {
        selectedEngineVersion: 'SelectedEngineVersion4',
        effectiveEngineVersion: 'EffectiveEngineVersion6',
      },
    },
    {
      name: 'Name4',
      state: WorkGroupState1Enum.ENABLED,
      description: 'Description0',
      creationTime: '2016-03-13T12:52:32.123Z',
      engineVersion: {
        selectedEngineVersion: 'SelectedEngineVersion4',
        effectiveEngineVersion: 'EffectiveEngineVersion6',
      },
    }
  ],
  nextToken: 'NextToken2',
};
```



