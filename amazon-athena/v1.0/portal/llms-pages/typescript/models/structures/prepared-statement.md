# Prepared Statement

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlByZXBhcmVkU3RhdGVtZW50

A prepared SQL statement for use with Athena.

*This model accepts additional fields of type unknown.*


# Interface Name

`PreparedStatement`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `statementName` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256`, *Pattern*: `[a-zA-Z_][a-zA-Z0-9_@:]{1,256}` |
| `queryStatement` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `262144` |
| `workGroupName` | `string \| undefined` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `description` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `lastModifiedTime` | `string \| undefined` | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { PreparedStatement } from 'amazon-athenalib';

const preparedStatement: PreparedStatement = {
  statementName: 'StatementName8',
  queryStatement: 'QueryStatement2',
  workGroupName: 'WorkGroupName2',
  description: 'Description4',
  lastModifiedTime: '2016-03-13T12:52:32.123Z',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



