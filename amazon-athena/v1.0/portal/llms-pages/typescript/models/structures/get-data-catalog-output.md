# Get Data Catalog Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkdldERhdGFDYXRhbG9nT3V0cHV0

*This model accepts additional fields of type unknown.*


# Interface Name

`GetDataCatalogOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dataCatalog` | [`DataCatalog2 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/data-catalog-2.md) | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { DataCatalogType1, GetDataCatalogOutput } from 'amazon-athenalib';

const getDataCatalogOutput: GetDataCatalogOutput = {
  dataCatalog: {
    name: 'Name4',
    type: DataCatalogType1.Glue,
    description: 'Description2',
    parameters: {
      additionalProperties: {
        'exampleAdditionalProperty': 'Parameters_additionalProperties2'
      },
    },
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



