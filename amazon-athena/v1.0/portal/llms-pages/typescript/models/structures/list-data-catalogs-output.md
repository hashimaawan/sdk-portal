# List Data Catalogs Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkxpc3REYXRhQ2F0YWxvZ3NPdXRwdXQ

*This model accepts additional fields of type unknown.*


# Interface Name

`ListDataCatalogsOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dataCatalogsSummary` | [`DataCatalogSummary[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/data-catalog-summary.md) | Optional | - |
| `nextToken` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { DataCatalogType2, ListDataCatalogsOutput } from 'amazon-athenalib';

const listDataCatalogsOutput: ListDataCatalogsOutput = {
  dataCatalogsSummary: [
    {
      catalogName: 'CatalogName4',
      type: DataCatalogType2.Hive,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      catalogName: 'CatalogName4',
      type: DataCatalogType2.Hive,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      catalogName: 'CatalogName4',
      type: DataCatalogType2.Hive,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  nextToken: 'NextToken0',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



