# Data Catalog

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkRhdGFDYXRhbG9n

<p>Contains information about a data catalog in an Amazon Web Services account.</p> <note> <p>In the Athena console, data catalogs are listed as "data sources" on the <b>Data sources</b> page under the <b>Data source name</b> column.</p> </note>
*This model accepts additional fields of type unknown.*


# Interface Name

`DataCatalog`


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
import { DataCatalog, DataCatalogType1 } from 'amazon-athenalib';

const dataCatalog: DataCatalog = {
  name: 'Name6',
  type: DataCatalogType1.Glue,
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



