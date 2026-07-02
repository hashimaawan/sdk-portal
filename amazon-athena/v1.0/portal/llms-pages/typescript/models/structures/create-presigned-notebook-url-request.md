# Create Presigned Notebook Url Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkNyZWF0ZVByZXNpZ25lZE5vdGVib29rVXJsUmVxdWVzdA

*This model accepts additional fields of type unknown.*


# Interface Name

`CreatePresignedNotebookUrlRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `sessionId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { CreatePresignedNotebookUrlRequest } from 'amazon-athenalib';

const createPresignedNotebookUrlRequest: CreatePresignedNotebookUrlRequest = {
  sessionId: 'SessionId0',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



