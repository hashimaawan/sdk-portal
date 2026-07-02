# Result Set Metadata

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlJlc3VsdFNldE1ldGFkYXRh

The metadata that describes the column structure and data types of a table of query results. To return a <code>ResultSetMetadata</code> object, use <a>GetQueryResults</a>.


# Interface Name

`ResultSetMetadata`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `columnInfo` | [`ColumnInfo[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/column-info.md) | Optional | - |


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
    },
    {
      name: 'Name6',
      type: 'Type6',
      catalogName: 'CatalogName0',
      schemaName: 'SchemaName0',
      tableName: 'TableName2',
      label: 'Label4',
      precision: 48,
    }
  ],
};
```



