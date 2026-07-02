# Create Presigned Notebook Url Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkNyZWF0ZVByZXNpZ25lZE5vdGVib29rVXJsUmVzcG9uc2U


# Interface Name

`CreatePresignedNotebookUrlResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `notebookUrl` | `string` | Required | - |
| `authToken` | `string` | Required | **Constraints**: *Maximum Length*: `2048` |
| `authTokenExpirationTime` | `number` | Required | - |


# Example

```ts
import { CreatePresignedNotebookUrlResponse } from 'amazon-athenalib';

const createPresignedNotebookUrlResponse: CreatePresignedNotebookUrlResponse = {
  notebookUrl: 'NotebookUrl0',
  authToken: 'AuthToken4',
  authTokenExpirationTime: 240,
};
```



