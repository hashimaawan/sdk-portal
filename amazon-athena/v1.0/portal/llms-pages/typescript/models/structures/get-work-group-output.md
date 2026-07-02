# Get Work Group Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkdldFdvcmtHcm91cE91dHB1dA


# Interface Name

`GetWorkGroupOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `workGroup` | [`WorkGroup2 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/work-group-2.md) | Optional | - |


# Example

```ts
import {
  EncryptionOption1Enum,
  GetWorkGroupOutput,
  S3AclOption1Enum,
  WorkGroupState3Enum,
} from 'amazon-athenalib';

const getWorkGroupOutput: GetWorkGroupOutput = {
  workGroup: {
    name: 'Name2',
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
    description: 'Description4',
    creationTime: '2016-03-13T12:52:32.123Z',
  },
};
```



