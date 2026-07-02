# Terminate Session Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlRlcm1pbmF0ZVNlc3Npb25SZXF1ZXN0

*This model accepts additional fields of type unknown.*


# Interface Name

`TerminateSessionRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `sessionId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { TerminateSessionRequest } from 'amazon-athenalib';

const terminateSessionRequest: TerminateSessionRequest = {
  sessionId: 'SessionId0',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



