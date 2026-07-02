# Column Info

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkNvbHVtbkluZm8

Information about the columns in a query execution result.


# Interface Name

`ColumnInfo`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `catalogName` | `string \| undefined` | Optional | - |
| `schemaName` | `string \| undefined` | Optional | - |
| `tableName` | `string \| undefined` | Optional | - |
| `name` | `string` | Required | - |
| `label` | `string \| undefined` | Optional | - |
| `type` | `string` | Required | - |
| `precision` | `number \| undefined` | Optional | - |
| `scale` | `number \| undefined` | Optional | - |
| `nullable` | [`ColumnNullable2Enum \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/enumerations/column-nullable-2.md) | Optional | - |
| `caseSensitive` | `boolean \| undefined` | Optional | - |


# Example

```ts
import { ColumnInfo } from 'amazon-athenalib';

const columnInfo: ColumnInfo = {
  name: 'Name8',
  type: 'Type8',
  catalogName: 'CatalogName2',
  schemaName: 'SchemaName2',
  tableName: 'TableName4',
  label: 'Label6',
  precision: 196,
};
```



