# Get Notebook Metadata Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkdldE5vdGVib29rTWV0YWRhdGFJbnB1dA


# Interface Name

`GetNotebookMetadataInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `notebookId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36`, *Pattern*: `[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}` |


# Example

```ts
import { GetNotebookMetadataInput } from 'amazon-athenalib';

const getNotebookMetadataInput: GetNotebookMetadataInput = {
  notebookId: 'NotebookId0',
};
```



