# Query Execution Context

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlF1ZXJ5RXhlY3V0aW9uQ29udGV4dA

The database and data catalog context in which the query execution occurs.

*This model accepts additional fields of type unknown.*


# Interface Name

`QueryExecutionContext`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `database` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` |
| `catalog` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { QueryExecutionContext } from 'amazon-athenalib';

const queryExecutionContext: QueryExecutionContext = {
  database: 'Database0',
  catalog: 'Catalog6',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



