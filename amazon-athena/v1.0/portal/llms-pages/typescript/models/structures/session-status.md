# Session Status

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlNlc3Npb25TdGF0dXM

Contains information about the status of a session.

*This model accepts additional fields of type unknown.*


# Interface Name

`SessionStatus`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `startDateTime` | `string \| undefined` | Optional | - |
| `lastModifiedDateTime` | `string \| undefined` | Optional | - |
| `endDateTime` | `string \| undefined` | Optional | - |
| `idleSinceDateTime` | `string \| undefined` | Optional | - |
| `state` | [`SessionState1 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/enumerations/session-state-1.md) | Optional | - |
| `stateChangeReason` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { SessionState1, SessionStatus } from 'amazon-athenalib';

const sessionStatus: SessionStatus = {
  startDateTime: '2016-03-13T12:52:32.123Z',
  lastModifiedDateTime: '2016-03-13T12:52:32.123Z',
  endDateTime: '2016-03-13T12:52:32.123Z',
  idleSinceDateTime: '2016-03-13T12:52:32.123Z',
  state: SessionState1.Idle,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



