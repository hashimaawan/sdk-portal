# Import Notebook Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkltcG9ydE5vdGVib29rSW5wdXQ


# Interface Name

`ImportNotebookInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `workGroup` | `string` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `name` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` |
| `payload` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `10485760` |
| `type` | [`NotebookType2Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/enumerations/notebook-type-2.md) | Required | - |
| `clientRequestToken` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36`, *Pattern*: `[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}` |


# Example

```ts
import { ImportNotebookInput, NotebookType2Enum } from 'amazon-athenalib';

const importNotebookInput: ImportNotebookInput = {
  workGroup: 'WorkGroup2',
  name: 'Name0',
  payload: 'Payload6',
  type: NotebookType2Enum.IPYNB,
  clientRequestToken: 'ClientRequestToken4',
};
```



