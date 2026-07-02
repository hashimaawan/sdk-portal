# Get Work Group Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkdldFdvcmtHcm91cElucHV0


# Interface Name

`GetWorkGroupInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `workGroup` | `string` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |


# Example

```ts
import { GetWorkGroupInput } from 'amazon-athenalib';

const getWorkGroupInput: GetWorkGroupInput = {
  workGroup: 'WorkGroup8',
};
```



