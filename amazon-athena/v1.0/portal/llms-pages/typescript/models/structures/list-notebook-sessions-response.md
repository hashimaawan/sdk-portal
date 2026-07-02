# List Notebook Sessions Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkxpc3ROb3RlYm9va1Nlc3Npb25zUmVzcG9uc2U


# Interface Name

`ListNotebookSessionsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `notebookSessionsList` | [`NotebookSessionSummary[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/notebook-session-summary.md) | Required | **Constraints**: *Minimum Items*: `0`, *Maximum Items*: `10` |
| `nextToken` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |


# Example

```ts
import { ListNotebookSessionsResponse } from 'amazon-athenalib';

const listNotebookSessionsResponse: ListNotebookSessionsResponse = {
  notebookSessionsList: [
    {
      sessionId: 'SessionId4',
      creationTime: '2016-03-13T12:52:32.123Z',
    }
  ],
  nextToken: 'NextToken0',
};
```



