# Get Database Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkdldERhdGFiYXNlSW5wdXQ

*This model accepts additional fields of type unknown.*


# Interface Name

`GetDatabaseInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `catalogName` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `databaseName` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { GetDatabaseInput } from 'amazon-athenalib';

const getDatabaseInput: GetDatabaseInput = {
  catalogName: 'CatalogName2',
  databaseName: 'DatabaseName2',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



