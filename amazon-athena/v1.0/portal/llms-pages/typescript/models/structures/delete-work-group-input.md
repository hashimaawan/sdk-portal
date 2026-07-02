# Delete Work Group Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkRlbGV0ZVdvcmtHcm91cElucHV0

*This model accepts additional fields of type unknown.*


# Interface Name

`DeleteWorkGroupInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `workGroup` | `string` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `recursiveDeleteOption` | `boolean \| undefined` | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { DeleteWorkGroupInput } from 'amazon-athenalib';

const deleteWorkGroupInput: DeleteWorkGroupInput = {
  workGroup: 'WorkGroup0',
  recursiveDeleteOption: false,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



