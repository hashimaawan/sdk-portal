# Delete Data Catalog Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkRlbGV0ZURhdGFDYXRhbG9nSW5wdXQ

*This model accepts additional fields of type unknown.*


# Interface Name

`DeleteDataCatalogInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { DeleteDataCatalogInput } from 'amazon-athenalib';

const deleteDataCatalogInput: DeleteDataCatalogInput = {
  name: 'Name2',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



