# List Data Catalogs Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkxpc3REYXRhQ2F0YWxvZ3NJbnB1dA

*This model accepts additional fields of type unknown.*


# Interface Name

`ListDataCatalogsInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `nextToken` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `maxResults` | `number \| undefined` | Optional | **Constraints**: `>= 2`, `<= 50` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { ListDataCatalogsInput } from 'amazon-athenalib';

const listDataCatalogsInput: ListDataCatalogsInput = {
  nextToken: 'NextToken8',
  maxResults: 50,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



