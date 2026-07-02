# Create Notebook Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkNyZWF0ZU5vdGVib29rSW5wdXQ

*This model accepts additional fields of type unknown.*


# Interface Name

`CreateNotebookInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `workGroup` | `string` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `name` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` |
| `clientRequestToken` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36`, *Pattern*: `[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { CreateNotebookInput } from 'amazon-athenalib';

const createNotebookInput: CreateNotebookInput = {
  workGroup: 'WorkGroup2',
  name: 'Name0',
  clientRequestToken: 'ClientRequestToken4',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



