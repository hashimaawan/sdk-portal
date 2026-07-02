# Unprocessed Prepared Statement Name

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlVucHJvY2Vzc2VkUHJlcGFyZWRTdGF0ZW1lbnROYW1l

The name of a prepared statement that could not be returned.

*This model accepts additional fields of type unknown.*


# Interface Name

`UnprocessedPreparedStatementName`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `statementName` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256`, *Pattern*: `[a-zA-Z_][a-zA-Z0-9_@:]{1,256}` |
| `errorCode` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `errorMessage` | `string \| undefined` | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { UnprocessedPreparedStatementName } from 'amazon-athenalib';

const unprocessedPreparedStatementName: UnprocessedPreparedStatementName = {
  statementName: 'StatementName8',
  errorCode: 'ErrorCode6',
  errorMessage: 'ErrorMessage6',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



