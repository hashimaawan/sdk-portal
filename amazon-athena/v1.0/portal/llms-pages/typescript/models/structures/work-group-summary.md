# Work Group Summary

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRldvcmtHcm91cFN1bW1hcnk

The summary information for the workgroup, which includes its name, state, description, and the date and time it was created.

*This model accepts additional fields of type unknown.*


# Interface Name

`WorkGroupSummary`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `string \| undefined` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `state` | [`WorkGroupState1 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/enumerations/work-group-state-1.md) | Optional | - |
| `description` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `1024` |
| `creationTime` | `string \| undefined` | Optional | - |
| `engineVersion` | [`EngineVersion1 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/engine-version-1.md) | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { WorkGroupState1, WorkGroupSummary } from 'amazon-athenalib';

const workGroupSummary: WorkGroupSummary = {
  name: 'Name4',
  state: WorkGroupState1.Enabled,
  description: 'Description8',
  creationTime: '2016-03-13T12:52:32.123Z',
  engineVersion: {
    selectedEngineVersion: 'SelectedEngineVersion4',
    effectiveEngineVersion: 'EffectiveEngineVersion6',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



