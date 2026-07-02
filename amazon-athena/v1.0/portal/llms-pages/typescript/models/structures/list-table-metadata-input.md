# List Table Metadata Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkxpc3RUYWJsZU1ldGFkYXRhSW5wdXQ

*This model accepts additional fields of type unknown.*


# Interface Name

`ListTableMetadataInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `catalogName` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `databaseName` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `expression` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `256` |
| `nextToken` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `maxResults` | `number \| undefined` | Optional | **Constraints**: `>= 1`, `<= 50` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { ListTableMetadataInput } from 'amazon-athenalib';

const listTableMetadataInput: ListTableMetadataInput = {
  catalogName: 'CatalogName2',
  databaseName: 'DatabaseName2',
  expression: 'Expression0',
  nextToken: 'NextToken8',
  maxResults: 50,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



