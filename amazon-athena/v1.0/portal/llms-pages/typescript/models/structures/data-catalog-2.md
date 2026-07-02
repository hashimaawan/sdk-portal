# Data Catalog 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkRhdGFDYXRhbG9nMg

*This model accepts additional fields of type unknown.*


# Interface Name

`DataCatalog2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `description` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `type` | [`DataCatalogType1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/enumerations/data-catalog-type-1.md) | Required | - |
| `parameters` | [`Parameters \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/parameters.md) | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { DataCatalog2, DataCatalogType1 } from 'amazon-athenalib';

const dataCatalog2: DataCatalog2 = {
  name: 'Name6',
  type: DataCatalogType1.Lambda,
  description: 'Description0',
  parameters: {
    additionalProperties: {
      'exampleAdditionalProperty': 'Parameters_additionalProperties2'
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



