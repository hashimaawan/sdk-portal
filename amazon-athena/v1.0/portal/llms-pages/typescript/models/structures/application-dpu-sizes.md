# Application DPU Sizes

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkFwcGxpY2F0aW9uRFBVU2l6ZXM

Contains the application runtime IDs and their supported DPU sizes.


# Interface Name

`ApplicationDPUSizes`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `applicationRuntimeId` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `supportedDPUSizes` | `number[] \| undefined` | Optional | - |


# Example

```ts
import { ApplicationDPUSizes } from 'amazon-athenalib';

const applicationDPUSizes: ApplicationDPUSizes = {
  applicationRuntimeId: 'ApplicationRuntimeId2',
  supportedDPUSizes: [
    57
  ],
};
```



