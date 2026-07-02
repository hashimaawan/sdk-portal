# Data Catalog Summary

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkRhdGFDYXRhbG9nU3VtbWFyeQ

The summary information for the data catalog, which includes its name and type.

*This model accepts additional fields of type unknown.*


# Interface Name

`DataCatalogSummary`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `catalogName` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `type` | [`DataCatalogType2 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/enumerations/data-catalog-type-2.md) | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { DataCatalogSummary, DataCatalogType2 } from 'amazon-athenalib';

const dataCatalogSummary: DataCatalogSummary = {
  catalogName: 'CatalogName2',
  type: DataCatalogType2.Hive,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



