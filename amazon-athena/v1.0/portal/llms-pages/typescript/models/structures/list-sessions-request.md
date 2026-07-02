# List Sessions Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkxpc3RTZXNzaW9uc1JlcXVlc3Q


# Interface Name

`ListSessionsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `workGroup` | `string` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `stateFilter` | [`SessionState3Enum \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/enumerations/session-state-3.md) | Optional | - |
| `maxResults` | `number \| undefined` | Optional | **Constraints**: `>= 1`, `<= 100` |
| `nextToken` | `string \| undefined` | Optional | **Constraints**: *Maximum Length*: `2048` |


# Example

```ts
import { ListSessionsRequest, SessionState3Enum } from 'amazon-athenalib';

const listSessionsRequest: ListSessionsRequest = {
  workGroup: 'WorkGroup8',
  stateFilter: SessionState3Enum.CREATING,
  maxResults: 100,
  nextToken: 'NextToken6',
};
```



