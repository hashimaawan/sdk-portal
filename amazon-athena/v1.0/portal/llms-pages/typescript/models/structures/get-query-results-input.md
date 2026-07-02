# Get Query Results Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkdldFF1ZXJ5UmVzdWx0c0lucHV0


# Interface Name

`GetQueryResultsInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `queryExecutionId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |
| `nextToken` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `maxResults` | `number \| undefined` | Optional | **Constraints**: `>= 1`, `<= 1000` |


# Example

```ts
import { GetQueryResultsInput } from 'amazon-athenalib';

const getQueryResultsInput: GetQueryResultsInput = {
  queryExecutionId: 'QueryExecutionId6',
  nextToken: 'NextToken2',
  maxResults: 42,
};
```



