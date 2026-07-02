# Update Work Group Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlVwZGF0ZVdvcmtHcm91cElucHV0


# Interface Name

`UpdateWorkGroupInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `workGroup` | `string` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `description` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `1024` |
| `configurationUpdates` | [`ConfigurationUpdates \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/configuration-updates.md) | Optional | - |
| `state` | [`WorkGroupState2Enum \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/enumerations/work-group-state-2.md) | Optional | - |


# Example

```ts
import {
  EncryptionOption1Enum,
  UpdateWorkGroupInput,
  WorkGroupState2Enum,
} from 'amazon-athenalib';

const updateWorkGroupInput: UpdateWorkGroupInput = {
  workGroup: 'WorkGroup0',
  description: 'Description8',
  configurationUpdates: {
    enforceWorkGroupConfiguration: false,
    resultConfigurationUpdates: {
      outputLocation: 'OutputLocation0',
      removeOutputLocation: false,
      encryptionConfiguration: {
        encryptionOption: EncryptionOption1Enum.SSES3,
        kmsKey: 'KmsKey6',
      },
      removeEncryptionConfiguration: false,
      expectedBucketOwner: 'ExpectedBucketOwner0',
    },
    publishCloudWatchMetricsEnabled: false,
    bytesScannedCutoffPerQuery: 10000000,
    removeBytesScannedCutoffPerQuery: false,
  },
  state: WorkGroupState2Enum.ENABLED,
};
```



