# Get Notebook Metadata Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkdldE5vdGVib29rTWV0YWRhdGFPdXRwdXQ

*This model accepts additional fields of type unknown.*


# Interface Name

`GetNotebookMetadataOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `notebookMetadata` | [`NotebookMetadata1 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/notebook-metadata-1.md) | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { GetNotebookMetadataOutput, NotebookType1 } from 'amazon-athenalib';

const getNotebookMetadataOutput: GetNotebookMetadataOutput = {
  notebookMetadata: {
    notebookId: 'NotebookId0',
    name: 'Name0',
    workGroup: 'WorkGroup2',
    creationTime: '2016-03-13T12:52:32.123Z',
    type: NotebookType1.Ipynb,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



