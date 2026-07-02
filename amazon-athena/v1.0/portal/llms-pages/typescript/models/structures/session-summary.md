# Session Summary

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlNlc3Npb25TdW1tYXJ5

Contains summary information about a session.

*This model accepts additional fields of type unknown.*


# Interface Name

`SessionSummary`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `sessionId` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `description` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `engineVersion` | [`EngineVersion1 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/engine-version-1.md) | Optional | - |
| `notebookVersion` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `status` | [`Status3 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/status-3.md) | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { SessionState1, SessionSummary } from 'amazon-athenalib';

const sessionSummary: SessionSummary = {
  sessionId: 'SessionId0',
  description: 'Description8',
  engineVersion: {
    selectedEngineVersion: 'SelectedEngineVersion4',
    effectiveEngineVersion: 'EffectiveEngineVersion6',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  notebookVersion: 'NotebookVersion2',
  status: {
    startDateTime: '2016-03-13T12:52:32.123Z',
    lastModifiedDateTime: '2016-03-13T12:52:32.123Z',
    endDateTime: '2016-03-13T12:52:32.123Z',
    idleSinceDateTime: '2016-03-13T12:52:32.123Z',
    state: SessionState1.Terminating,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



