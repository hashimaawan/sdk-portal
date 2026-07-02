# Start Session Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlN0YXJ0U2Vzc2lvblJlc3BvbnNl

*This model accepts additional fields of type unknown.*


# Interface Name

`StartSessionResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `sessionId` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `state` | [`SessionState1 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/enumerations/session-state-1.md) | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { SessionState1, StartSessionResponse } from 'amazon-athenalib';

const startSessionResponse: StartSessionResponse = {
  sessionId: 'SessionId4',
  state: SessionState1.Creating,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



