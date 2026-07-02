# Create Data Catalog Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkNyZWF0ZURhdGFDYXRhbG9nSW5wdXQ


# Interface Name

`CreateDataCatalogInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `type` | [`DataCatalogType1Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/enumerations/data-catalog-type-1.md) | Required | - |
| `description` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `parameters` | [`Parameters \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/parameters.md) | Optional | - |
| `tags` | [`Tag[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/tag.md) | Optional | - |


# Example

```ts
import {
  CreateDataCatalogInput,
  DataCatalogType1Enum,
} from 'amazon-athenalib';

const createDataCatalogInput: CreateDataCatalogInput = {
  name: 'Name6',
  type: DataCatalogType1Enum.GLUE,
  description: 'Description2',
  parameters: {},
  tags: [
    {
      key: 'Key0',
      value: 'Value6',
    },
    {
      key: 'Key0',
      value: 'Value6',
    },
    {
      key: 'Key0',
      value: 'Value6',
    }
  ],
};
```



