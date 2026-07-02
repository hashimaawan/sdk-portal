# Table Metadata 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlRhYmxlTWV0YWRhdGEy


# Interface Name

`TableMetadata2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `createTime` | `string \| undefined` | Optional | - |
| `lastAccessTime` | `string \| undefined` | Optional | - |
| `tableType` | `string \| undefined` | Optional | **Constraints**: *Maximum Length*: `255` |
| `columns` | [`Column[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/column.md) | Optional | - |
| `partitionKeys` | [`Column[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/column.md) | Optional | - |
| `parameters` | [`Parameters \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/parameters.md) | Optional | - |


# Example

```ts
import { TableMetadata2 } from 'amazon-athenalib';

const tableMetadata2: TableMetadata2 = {
  name: 'Name8',
  createTime: '2016-03-13T12:52:32.123Z',
  lastAccessTime: '2016-03-13T12:52:32.123Z',
  tableType: 'TableType6',
  columns: [
    {
      name: 'Name0',
      type: 'Type0',
      comment: 'Comment4',
    },
    {
      name: 'Name0',
      type: 'Type0',
      comment: 'Comment4',
    }
  ],
  partitionKeys: [
    {
      name: 'Name6',
      type: 'Type6',
      comment: 'Comment0',
    },
    {
      name: 'Name6',
      type: 'Type6',
      comment: 'Comment0',
    }
  ],
};
```



