# List Application DPU Sizes Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkxpc3RBcHBsaWNhdGlvbkRQVVNpemVzT3V0cHV0

*This model accepts additional fields of type unknown.*


# Interface Name

`ListApplicationDpuSizesOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `applicationDpuSizes` | [`ApplicationDpuSizes[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/application-dpu-sizes.md) | Optional | - |
| `nextToken` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { ListApplicationDpuSizesOutput } from 'amazon-athenalib';

const listApplicationDpuSizesOutput: ListApplicationDpuSizesOutput = {
  applicationDpuSizes: [
    {
      applicationRuntimeId: 'ApplicationRuntimeId0',
      supportedDpuSizes: [
        113,
        114
      ],
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      applicationRuntimeId: 'ApplicationRuntimeId0',
      supportedDpuSizes: [
        113,
        114
      ],
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  nextToken: 'NextToken0',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



