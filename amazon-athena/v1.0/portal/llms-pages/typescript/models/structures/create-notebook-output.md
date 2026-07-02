# Create Notebook Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkNyZWF0ZU5vdGVib29rT3V0cHV0

*This model accepts additional fields of type unknown.*


# Interface Name

`CreateNotebookOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `notebookId` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36`, *Pattern*: `[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { CreateNotebookOutput } from 'amazon-athenalib';

const createNotebookOutput: CreateNotebookOutput = {
  notebookId: 'NotebookId6',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



