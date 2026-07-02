# Result Set Metadata 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlJlc3VsdFNldE1ldGFkYXRhMg

*This model accepts additional fields of type unknown.*


# Interface Name

`ResultSetMetadata2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `columnInfo` | [`ColumnInfo[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/column-info.md) | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { ResultSetMetadata2 } from 'amazon-athenalib';

const resultSetMetadata2: ResultSetMetadata2 = {
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



