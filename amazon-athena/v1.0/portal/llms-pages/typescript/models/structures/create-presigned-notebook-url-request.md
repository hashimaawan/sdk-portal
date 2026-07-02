# Create Presigned Notebook Url Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkNyZWF0ZVByZXNpZ25lZE5vdGVib29rVXJsUmVxdWVzdA


# Interface Name

`CreatePresignedNotebookUrlRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `sessionId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |


# Example

```ts
import { CreatePresignedNotebookUrlRequest } from 'amazon-athenalib';

const createPresignedNotebookUrlRequest: CreatePresignedNotebookUrlRequest = {
  sessionId: 'SessionId0',
};
```



