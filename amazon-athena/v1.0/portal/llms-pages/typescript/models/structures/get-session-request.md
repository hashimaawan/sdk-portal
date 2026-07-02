# Get Session Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkdldFNlc3Npb25SZXF1ZXN0


# Interface Name

`GetSessionRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `sessionId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |


# Example

```ts
import { GetSessionRequest } from 'amazon-athenalib';

const getSessionRequest: GetSessionRequest = {
  sessionId: 'SessionId2',
};
```



