# Status 3

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlN0YXR1czM


# Interface Name

`Status3`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `startDateTime` | `string \| undefined` | Optional | - |
| `lastModifiedDateTime` | `string \| undefined` | Optional | - |
| `endDateTime` | `string \| undefined` | Optional | - |
| `idleSinceDateTime` | `string \| undefined` | Optional | - |
| `state` | [`SessionState1Enum \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/enumerations/session-state-1.md) | Optional | - |
| `stateChangeReason` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |


# Example

```ts
import { SessionState1Enum, Status3 } from 'amazon-athenalib';

const status3: Status3 = {
  startDateTime: '2016-03-13T12:52:32.123Z',
  lastModifiedDateTime: '2016-03-13T12:52:32.123Z',
  endDateTime: '2016-03-13T12:52:32.123Z',
  idleSinceDateTime: '2016-03-13T12:52:32.123Z',
  state: SessionState1Enum.CREATING,
};
```



