# Export Notebook Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkV4cG9ydE5vdGVib29rT3V0cHV0

*This model accepts additional fields of type unknown.*


# Interface Name

`ExportNotebookOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `notebookMetadata` | [`NotebookMetadata1 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/notebook-metadata-1.md) | Optional | - |
| `payload` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `10485760` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { ExportNotebookOutput, NotebookType1 } from 'amazon-athenalib';

const exportNotebookOutput: ExportNotebookOutput = {
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
  payload: 'Payload2',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



