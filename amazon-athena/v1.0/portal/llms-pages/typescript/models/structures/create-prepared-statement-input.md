# Create Prepared Statement Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkNyZWF0ZVByZXBhcmVkU3RhdGVtZW50SW5wdXQ


# Interface Name

`CreatePreparedStatementInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `statementName` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256`, *Pattern*: `[a-zA-Z_][a-zA-Z0-9_@:]{1,256}` |
| `workGroup` | `string` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `queryStatement` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `262144` |
| `description` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |


# Example

```ts
import { CreatePreparedStatementInput } from 'amazon-athenalib';

const createPreparedStatementInput: CreatePreparedStatementInput = {
  statementName: 'StatementName2',
  workGroup: 'WorkGroup6',
  queryStatement: 'QueryStatement6',
  description: 'Description2',
};
```



