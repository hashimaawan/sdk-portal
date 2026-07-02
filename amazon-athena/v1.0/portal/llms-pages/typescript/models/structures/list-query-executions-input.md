# List Query Executions Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkxpc3RRdWVyeUV4ZWN1dGlvbnNJbnB1dA


# Interface Name

`ListQueryExecutionsInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `nextToken` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `maxResults` | `number \| undefined` | Optional | **Constraints**: `>= 0`, `<= 50` |
| `workGroup` | `string \| undefined` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |


# Example

```ts
import { ListQueryExecutionsInput } from 'amazon-athenalib';

const listQueryExecutionsInput: ListQueryExecutionsInput = {
  nextToken: 'NextToken2',
  maxResults: 34,
  workGroup: 'WorkGroup4',
};
```



