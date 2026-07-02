# Get Work Group Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkdldFdvcmtHcm91cElucHV0

*This model accepts additional fields of type unknown.*


# Interface Name

`GetWorkGroupInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `workGroup` | `string` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { GetWorkGroupInput } from 'amazon-athenalib';

const getWorkGroupInput: GetWorkGroupInput = {
  workGroup: 'WorkGroup8',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



