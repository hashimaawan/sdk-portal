# Prepared Statement Summary

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlByZXBhcmVkU3RhdGVtZW50U3VtbWFyeQ

The name and last modified time of the prepared statement.


# Interface Name

`PreparedStatementSummary`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `statementName` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256`, *Pattern*: `[a-zA-Z_][a-zA-Z0-9_@:]{1,256}` |
| `lastModifiedTime` | `string \| undefined` | Optional | - |


# Example

```ts
import { PreparedStatementSummary } from 'amazon-athenalib';

const preparedStatementSummary: PreparedStatementSummary = {
  statementName: 'StatementName4',
  lastModifiedTime: '2016-03-13T12:52:32.123Z',
};
```



