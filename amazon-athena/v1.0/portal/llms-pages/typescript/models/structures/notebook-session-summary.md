# Notebook Session Summary

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRk5vdGVib29rU2Vzc2lvblN1bW1hcnk

Contains the notebook session ID and notebook session creation time.


# Interface Name

`NotebookSessionSummary`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `sessionId` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `creationTime` | `string \| undefined` | Optional | - |


# Example

```ts
import { NotebookSessionSummary } from 'amazon-athenalib';

const notebookSessionSummary: NotebookSessionSummary = {
  sessionId: 'SessionId0',
  creationTime: '2016-03-13T12:52:32.123Z',
};
```



