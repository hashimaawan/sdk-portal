# List Notebook Metadata Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkxpc3ROb3RlYm9va01ldGFkYXRhSW5wdXQ

*This model accepts additional fields of type unknown.*


# Interface Name

`ListNotebookMetadataInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `filters` | [`Filters \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/filters.md) | Optional | - |
| `nextToken` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `maxResults` | `number \| undefined` | Optional | **Constraints**: `>= 1`, `<= 50` |
| `workGroup` | `string` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { ListNotebookMetadataInput } from 'amazon-athenalib';

const listNotebookMetadataInput: ListNotebookMetadataInput = {
  workGroup: 'WorkGroup4',
  filters: {
    name: 'Name2',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  nextToken: 'NextToken2',
  maxResults: 50,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



