# Terminate Session Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlRlcm1pbmF0ZVNlc3Npb25SZXNwb25zZQ

*This model accepts additional fields of type unknown.*


# Interface Name

`TerminateSessionResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `state` | [`SessionState1 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/enumerations/session-state-1.md) | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { SessionState1, TerminateSessionResponse } from 'amazon-athenalib';

const terminateSessionResponse: TerminateSessionResponse = {
  state: SessionState1.Creating,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



