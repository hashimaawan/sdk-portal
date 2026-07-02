# Notebook Metadata

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRk5vdGVib29rTWV0YWRhdGE

Contains metadata for notebook, including the notebook name, ID, workgroup, and time created.

*This model accepts additional fields of type unknown.*


# Interface Name

`NotebookMetadata`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `notebookId` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36`, *Pattern*: `[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}` |
| `name` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` |
| `workGroup` | `string \| undefined` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `creationTime` | `string \| undefined` | Optional | - |
| `type` | [`NotebookType1 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/enumerations/notebook-type-1.md) | Optional | - |
| `lastModifiedTime` | `string \| undefined` | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { NotebookMetadata, NotebookType1 } from 'amazon-athenalib';

const notebookMetadata: NotebookMetadata = {
  notebookId: 'NotebookId0',
  name: 'Name0',
  workGroup: 'WorkGroup2',
  creationTime: '2016-03-13T12:52:32.123Z',
  type: NotebookType1.Ipynb,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



