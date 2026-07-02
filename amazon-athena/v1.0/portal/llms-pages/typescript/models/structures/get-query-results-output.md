# Get Query Results Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkdldFF1ZXJ5UmVzdWx0c091dHB1dA


# Interface Name

`GetQueryResultsOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `updateCount` | `number \| undefined` | Optional | - |
| `resultSet` | [`ResultSet2 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/result-set-2.md) | Optional | - |
| `nextToken` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |


# Example

```ts
import { GetQueryResultsOutput } from 'amazon-athenalib';

const getQueryResultsOutput: GetQueryResultsOutput = {
  updateCount: 60,
  resultSet: {
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
      },
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
  },
  nextToken: 'NextToken0',
};
```



