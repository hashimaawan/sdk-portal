# Application DPU Sizes

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkFwcGxpY2F0aW9uRFBVU2l6ZXM

Contains the application runtime IDs and their supported DPU sizes.

*This model accepts additional fields of type unknown.*


# Interface Name

`ApplicationDpuSizes`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `applicationRuntimeId` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `supportedDpuSizes` | `number[] \| undefined` | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { ApplicationDpuSizes } from 'amazon-athenalib';

const applicationDpuSizes: ApplicationDpuSizes = {
  applicationRuntimeId: 'ApplicationRuntimeId4',
  supportedDpuSizes: [
    17,
    18
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



