# Update Data Catalog Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlVwZGF0ZURhdGFDYXRhbG9nSW5wdXQ

*This model accepts additional fields of type unknown.*


# Interface Name

`UpdateDataCatalogInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `type` | [`DataCatalogType3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/enumerations/data-catalog-type-3.md) | Required | - |
| `description` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `parameters` | [`Parameters \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/parameters.md) | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { DataCatalogType3, UpdateDataCatalogInput } from 'amazon-athenalib';

const updateDataCatalogInput: UpdateDataCatalogInput = {
  name: 'Name4',
  type: DataCatalogType3.Glue,
  description: 'Description2',
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



