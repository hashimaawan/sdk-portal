# Update Notebook Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlVwZGF0ZU5vdGVib29rSW5wdXQ

*This model accepts additional fields of type unknown.*


# Interface Name

`UpdateNotebookInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `notebookId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36`, *Pattern*: `[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}` |
| `payload` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `10485760` |
| `type` | [`NotebookType2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/enumerations/notebook-type-2.md) | Required | - |
| `sessionId` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `clientRequestToken` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36`, *Pattern*: `[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { NotebookType2, UpdateNotebookInput } from 'amazon-athenalib';

const updateNotebookInput: UpdateNotebookInput = {
  notebookId: 'NotebookId8',
  payload: 'Payload4',
  type: NotebookType2.Ipynb,
  sessionId: 'SessionId0',
  clientRequestToken: 'ClientRequestToken2',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



