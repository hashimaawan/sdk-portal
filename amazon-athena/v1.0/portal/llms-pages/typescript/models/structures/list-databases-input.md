# List Databases Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkxpc3REYXRhYmFzZXNJbnB1dA


# Interface Name

`ListDatabasesInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `catalogName` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `nextToken` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `maxResults` | `number \| undefined` | Optional | **Constraints**: `>= 1`, `<= 50` |


# Example

```ts
import { ListDatabasesInput } from 'amazon-athenalib';

const listDatabasesInput: ListDatabasesInput = {
  catalogName: 'CatalogName4',
  nextToken: 'NextToken0',
  maxResults: 50,
};
```



