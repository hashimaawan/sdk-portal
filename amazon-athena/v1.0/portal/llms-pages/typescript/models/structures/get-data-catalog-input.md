# Get Data Catalog Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkdldERhdGFDYXRhbG9nSW5wdXQ

*This model accepts additional fields of type unknown.*


# Interface Name

`GetDataCatalogInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { GetDataCatalogInput } from 'amazon-athenalib';

const getDataCatalogInput: GetDataCatalogInput = {
  name: 'Name6',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



