# List Application DPU Sizes Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkxpc3RBcHBsaWNhdGlvbkRQVVNpemVzT3V0cHV0


# Interface Name

`ListApplicationDPUSizesOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `applicationDPUSizes` | [`ApplicationDPUSizes[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/application-dpu-sizes.md) | Optional | - |
| `nextToken` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |


# Example

```ts
import { ListApplicationDPUSizesOutput } from 'amazon-athenalib';

const listApplicationDPUSizesOutput: ListApplicationDPUSizesOutput = {
  applicationDPUSizes: [
    {
      applicationRuntimeId: 'ApplicationRuntimeId0',
      supportedDPUSizes: [
        113,
        114
      ],
    },
    {
      applicationRuntimeId: 'ApplicationRuntimeId0',
      supportedDPUSizes: [
        113,
        114
      ],
    }
  ],
  nextToken: 'NextToken0',
};
```



