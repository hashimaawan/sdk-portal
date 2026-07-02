# Work Group 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRldvcmtHcm91cDI


# Interface Name

`WorkGroup2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `string` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `state` | [`WorkGroupState3Enum \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/enumerations/work-group-state-3.md) | Optional | - |
| `configuration` | [`MConfiguration \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/configuration.md) | Optional | - |
| `description` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `1024` |
| `creationTime` | `string \| undefined` | Optional | - |


# Example

```ts
import {
  EncryptionOption1Enum,
  S3AclOption1Enum,
  WorkGroup2,
  WorkGroupState3Enum,
} from 'amazon-athenalib';

const workGroup2: WorkGroup2 = {
  name: 'Name0',
  state: WorkGroupState3Enum.ENABLED,
  configuration: {
    resultConfiguration: {
      outputLocation: 'OutputLocation0',
      encryptionConfiguration: {
        encryptionOption: EncryptionOption1Enum.SSES3,
        kmsKey: 'KmsKey6',
      },
      expectedBucketOwner: 'ExpectedBucketOwner0',
      aclConfiguration: {
        s3AclOption: S3AclOption1Enum.BUCKETOWNERFULLCONTROL,
      },
    },
    enforceWorkGroupConfiguration: false,
    publishCloudWatchMetricsEnabled: false,
    bytesScannedCutoffPerQuery: 10000000,
    requesterPaysEnabled: false,
  },
  description: 'Description6',
  creationTime: '2016-03-13T12:52:32.123Z',
};
```



