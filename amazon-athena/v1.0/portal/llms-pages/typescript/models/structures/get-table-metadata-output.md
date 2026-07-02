# Get Table Metadata Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkdldFRhYmxlTWV0YWRhdGFPdXRwdXQ

*This model accepts additional fields of type unknown.*


# Interface Name

`GetTableMetadataOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `tableMetadata` | [`TableMetadata2 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/table-metadata-2.md) | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { GetTableMetadataOutput } from 'amazon-athenalib';

const getTableMetadataOutput: GetTableMetadataOutput = {
  tableMetadata: {
    name: 'Name6',
    createTime: '2016-03-13T12:52:32.123Z',
    lastAccessTime: '2016-03-13T12:52:32.123Z',
    tableType: 'TableType0',
    columns: [
      {
        name: 'Name0',
        type: 'Type0',
        comment: 'Comment4',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      {
        name: 'Name0',
        type: 'Type0',
        comment: 'Comment4',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      {
        name: 'Name0',
        type: 'Type0',
        comment: 'Comment4',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      }
    ],
    partitionKeys: [
      {
        name: 'Name6',
        type: 'Type6',
        comment: 'Comment0',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      }
    ],
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



