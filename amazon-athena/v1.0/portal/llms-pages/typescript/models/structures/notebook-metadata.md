# Notebook Metadata

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRk5vdGVib29rTWV0YWRhdGE

Contains metadata for notebook, including the notebook name, ID, workgroup, and time created.


# Interface Name

`NotebookMetadata`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `notebookId` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36`, *Pattern*: `[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}` |
| `name` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` |
| `workGroup` | `string \| undefined` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `creationTime` | `string \| undefined` | Optional | - |
| `type` | [`NotebookType1Enum \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/enumerations/notebook-type-1.md) | Optional | - |
| `lastModifiedTime` | `string \| undefined` | Optional | - |


# Example

```ts
import { NotebookMetadata, NotebookType1Enum } from 'amazon-athenalib';

const notebookMetadata: NotebookMetadata = {
  notebookId: 'NotebookId0',
  name: 'Name0',
  workGroup: 'WorkGroup2',
  creationTime: '2016-03-13T12:52:32.123Z',
  type: NotebookType1Enum.IPYNB,
};
```



