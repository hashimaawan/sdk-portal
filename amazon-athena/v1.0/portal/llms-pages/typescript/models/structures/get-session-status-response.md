# Get Session Status Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkdldFNlc3Npb25TdGF0dXNSZXNwb25zZQ

*This model accepts additional fields of type unknown.*


# Interface Name

`GetSessionStatusResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `sessionId` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `status` | [`Status3 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/status-3.md) | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { GetSessionStatusResponse, SessionState1 } from 'amazon-athenalib';

const getSessionStatusResponse: GetSessionStatusResponse = {
  sessionId: 'SessionId4',
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



