# List Data Catalogs Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkxpc3REYXRhQ2F0YWxvZ3NPdXRwdXQ


# Interface Name

`ListDataCatalogsOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dataCatalogsSummary` | [`DataCatalogSummary[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/data-catalog-summary.md) | Optional | - |
| `nextToken` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |


# Example

```ts
import {
  DataCatalogType2Enum,
  ListDataCatalogsOutput,
} from 'amazon-athenalib';

const listDataCatalogsOutput: ListDataCatalogsOutput = {
  dataCatalogsSummary: [
    {
      catalogName: 'CatalogName4',
      type: DataCatalogType2Enum.HIVE,
    },
    {
      catalogName: 'CatalogName4',
      type: DataCatalogType2Enum.HIVE,
    },
    {
      catalogName: 'CatalogName4',
      type: DataCatalogType2Enum.HIVE,
    }
  ],
  nextToken: 'NextToken0',
};
```



