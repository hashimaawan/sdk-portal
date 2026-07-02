# List Notebook Metadata Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkxpc3ROb3RlYm9va01ldGFkYXRhT3V0cHV0


# Interface Name

`ListNotebookMetadataOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `nextToken` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `notebookMetadataList` | [`NotebookMetadata[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/notebook-metadata.md) | Optional | - |


# Example

```ts
import {
  ListNotebookMetadataOutput,
  NotebookType1Enum,
} from 'amazon-athenalib';

const listNotebookMetadataOutput: ListNotebookMetadataOutput = {
  nextToken: 'NextToken2',
  notebookMetadataList: [
    {
      notebookId: 'NotebookId4',
      name: 'Name4',
      workGroup: 'WorkGroup6',
      creationTime: '2016-03-13T12:52:32.123Z',
      type: NotebookType1Enum.IPYNB,
    }
  ],
};
```



