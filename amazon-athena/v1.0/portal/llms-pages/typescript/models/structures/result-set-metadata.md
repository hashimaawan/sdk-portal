# Result Set Metadata

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlJlc3VsdFNldE1ldGFkYXRh

The metadata that describes the column structure and data types of a table of query results. To return a <code>ResultSetMetadata</code> object, use <a>GetQueryResults</a>.

*This model accepts additional fields of type unknown.*


# Interface Name

`ResultSetMetadata`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `columnInfo` | [`ColumnInfo[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/column-info.md) | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { ResultSetMetadata } from 'amazon-athenalib';

const resultSetMetadata: ResultSetMetadata = {
  columnInfo: [
    {
      name: 'Name6',
      type: 'Type6',
      catalogName: 'CatalogName0',
      schemaName: 'SchemaName0',
      tableName: 'TableName2',
      label: 'Label4',
      precision: 48,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      name: 'Name6',
      type: 'Type6',
      catalogName: 'CatalogName0',
      schemaName: 'SchemaName0',
      tableName: 'TableName2',
      label: 'Label4',
      precision: 48,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



