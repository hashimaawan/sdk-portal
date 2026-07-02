# Result Set 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlJlc3VsdFNldDI

*This model accepts additional fields of type unknown.*


# Interface Name

`ResultSet2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `rows` | [`Row[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/row.md) | Optional | - |
| `resultSetMetadata` | [`ResultSetMetadata2 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/result-set-metadata-2.md) | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { ResultSet2 } from 'amazon-athenalib';

const resultSet2: ResultSet2 = {
  rows: [
    {
      data: [
        {
          varCharValue: 'VarCharValue8',
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        {
          varCharValue: 'VarCharValue8',
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        }
      ],
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
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



