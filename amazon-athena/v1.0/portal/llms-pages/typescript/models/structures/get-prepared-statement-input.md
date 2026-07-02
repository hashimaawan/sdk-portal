# Get Prepared Statement Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkdldFByZXBhcmVkU3RhdGVtZW50SW5wdXQ

*This model accepts additional fields of type unknown.*


# Interface Name

`GetPreparedStatementInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `statementName` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256`, *Pattern*: `[a-zA-Z_][a-zA-Z0-9_@:]{1,256}` |
| `workGroup` | `string` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { GetPreparedStatementInput } from 'amazon-athenalib';

const getPreparedStatementInput: GetPreparedStatementInput = {
  statementName: 'StatementName6',
  workGroup: 'WorkGroup0',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



