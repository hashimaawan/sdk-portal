# List Sessions Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkxpc3RTZXNzaW9uc1Jlc3BvbnNl


# Interface Name

`ListSessionsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `nextToken` | `string \| undefined` | Optional | **Constraints**: *Maximum Length*: `2048` |
| `sessions` | [`SessionSummary[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/session-summary.md) | Optional | **Constraints**: *Minimum Items*: `0`, *Maximum Items*: `100` |


# Example

```ts
import { ListSessionsResponse, SessionState1Enum } from 'amazon-athenalib';

const listSessionsResponse: ListSessionsResponse = {
  nextToken: 'NextToken6',
  sessions: [
    {
      sessionId: 'SessionId6',
      description: 'Description4',
      engineVersion: {
        selectedEngineVersion: 'SelectedEngineVersion4',
        effectiveEngineVersion: 'EffectiveEngineVersion6',
      },
      notebookVersion: 'NotebookVersion6',
      status: {
        startDateTime: '2016-03-13T12:52:32.123Z',
        lastModifiedDateTime: '2016-03-13T12:52:32.123Z',
        endDateTime: '2016-03-13T12:52:32.123Z',
        idleSinceDateTime: '2016-03-13T12:52:32.123Z',
        state: SessionState1Enum.TERMINATING,
      },
    },
    {
      sessionId: 'SessionId6',
      description: 'Description4',
      engineVersion: {
        selectedEngineVersion: 'SelectedEngineVersion4',
        effectiveEngineVersion: 'EffectiveEngineVersion6',
      },
      notebookVersion: 'NotebookVersion6',
      status: {
        startDateTime: '2016-03-13T12:52:32.123Z',
        lastModifiedDateTime: '2016-03-13T12:52:32.123Z',
        endDateTime: '2016-03-13T12:52:32.123Z',
        idleSinceDateTime: '2016-03-13T12:52:32.123Z',
        state: SessionState1Enum.TERMINATING,
      },
    },
    {
      sessionId: 'SessionId6',
      description: 'Description4',
      engineVersion: {
        selectedEngineVersion: 'SelectedEngineVersion4',
        effectiveEngineVersion: 'EffectiveEngineVersion6',
      },
      notebookVersion: 'NotebookVersion6',
      status: {
        startDateTime: '2016-03-13T12:52:32.123Z',
        lastModifiedDateTime: '2016-03-13T12:52:32.123Z',
        endDateTime: '2016-03-13T12:52:32.123Z',
        idleSinceDateTime: '2016-03-13T12:52:32.123Z',
        state: SessionState1Enum.TERMINATING,
      },
    }
  ],
};
```



