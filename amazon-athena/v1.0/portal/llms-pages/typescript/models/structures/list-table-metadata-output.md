# List Table Metadata Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkxpc3RUYWJsZU1ldGFkYXRhT3V0cHV0


# Interface Name

`ListTableMetadataOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `tableMetadataList` | [`TableMetadata[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/table-metadata.md) | Optional | - |
| `nextToken` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |


# Example

```ts
import { ListTableMetadataOutput } from 'amazon-athenalib';

const listTableMetadataOutput: ListTableMetadataOutput = {
  tableMetadataList: [
    {
      name: 'Name2',
      createTime: '2016-03-13T12:52:32.123Z',
      lastAccessTime: '2016-03-13T12:52:32.123Z',
      tableType: 'TableType2',
      columns: [
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
        },
        {
          name: 'Name6',
          type: 'Type6',
          comment: 'Comment0',
        }
      ],
    },
    {
      name: 'Name2',
      createTime: '2016-03-13T12:52:32.123Z',
      lastAccessTime: '2016-03-13T12:52:32.123Z',
      tableType: 'TableType2',
      columns: [
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
        },
        {
          name: 'Name6',
          type: 'Type6',
          comment: 'Comment0',
        }
      ],
    }
  ],
  nextToken: 'NextToken0',
};
```



