# Get Data Catalog Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkdldERhdGFDYXRhbG9nT3V0cHV0


# Interface Name

`GetDataCatalogOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dataCatalog` | [`DataCatalog2 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/data-catalog-2.md) | Optional | - |


# Example

```ts
import { DataCatalogType1Enum, GetDataCatalogOutput } from 'amazon-athenalib';

const getDataCatalogOutput: GetDataCatalogOutput = {
  dataCatalog: {
    name: 'Name4',
    type: DataCatalogType1Enum.GLUE,
    description: 'Description2',
    parameters: {},
  },
};
```



