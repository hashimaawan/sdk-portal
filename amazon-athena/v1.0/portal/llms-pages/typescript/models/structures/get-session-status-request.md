# Get Session Status Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkdldFNlc3Npb25TdGF0dXNSZXF1ZXN0

*This model accepts additional fields of type unknown.*


# Interface Name

`GetSessionStatusRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `sessionId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { GetSessionStatusRequest } from 'amazon-athenalib';

const getSessionStatusRequest: GetSessionStatusRequest = {
  sessionId: 'SessionId6',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



