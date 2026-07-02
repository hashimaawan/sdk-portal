# List Sessions Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkxpc3RTZXNzaW9uc1JlcXVlc3Q

*This model accepts additional fields of type unknown.*


# Interface Name

`ListSessionsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `workGroup` | `string` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `stateFilter` | [`SessionState3 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/enumerations/session-state-3.md) | Optional | - |
| `maxResults` | `number \| undefined` | Optional | **Constraints**: `>= 1`, `<= 100` |
| `nextToken` | `string \| undefined` | Optional | **Constraints**: *Maximum Length*: `2048` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { ListSessionsRequest, SessionState3 } from 'amazon-athenalib';

const listSessionsRequest: ListSessionsRequest = {
  workGroup: 'WorkGroup8',
  stateFilter: SessionState3.Creating,
  maxResults: 100,
  nextToken: 'NextToken6',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



