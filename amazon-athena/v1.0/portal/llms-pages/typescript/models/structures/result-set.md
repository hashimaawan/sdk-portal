# Result Set

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlJlc3VsdFNldA

The metadata and rows that make up a query result set. The metadata describes the column structure and data types. To return a <code>ResultSet</code> object, use <a>GetQueryResults</a>.


# Interface Name

`ResultSet`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `rows` | [`Row[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/row.md) | Optional | - |
| `resultSetMetadata` | [`ResultSetMetadata2 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/result-set-metadata-2.md) | Optional | - |


# Example

```ts
import { ResultSet } from 'amazon-athenalib';

const resultSet: ResultSet = {
  rows: [
    {
      data: [
        {
          varCharValue: 'VarCharValue8',
        },
        {
          varCharValue: 'VarCharValue8',
        }
      ],
    }
  ],
  resultSetMetadata: {
    columnInfo: [
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
  },
};
```



