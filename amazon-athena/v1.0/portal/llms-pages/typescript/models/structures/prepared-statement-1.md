# Prepared Statement 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlByZXBhcmVkU3RhdGVtZW50MQ

*This model accepts additional fields of type unknown.*


# Interface Name

`PreparedStatement1`


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
import { PreparedStatement1 } from 'amazon-athenalib';

const preparedStatement1: PreparedStatement1 = {
  statementName: 'StatementName6',
  queryStatement: 'QueryStatement0',
  workGroupName: 'WorkGroupName0',
  description: 'Description8',
  lastModifiedTime: '2016-03-13T12:52:32.123Z',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



