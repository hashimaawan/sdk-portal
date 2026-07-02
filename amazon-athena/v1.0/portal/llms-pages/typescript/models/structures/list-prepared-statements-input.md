# List Prepared Statements Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkxpc3RQcmVwYXJlZFN0YXRlbWVudHNJbnB1dA


# Interface Name

`ListPreparedStatementsInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `workGroup` | `string` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `nextToken` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `maxResults` | `number \| undefined` | Optional | **Constraints**: `>= 1`, `<= 50` |


# Example

```ts
import { ListPreparedStatementsInput } from 'amazon-athenalib';

const listPreparedStatementsInput: ListPreparedStatementsInput = {
  workGroup: 'WorkGroup2',
  nextToken: 'NextToken0',
  maxResults: 50,
};
```



