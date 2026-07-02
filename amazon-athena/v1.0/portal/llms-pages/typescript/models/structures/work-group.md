# Work Group

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRldvcmtHcm91cA

A workgroup, which contains a name, description, creation time, state, and other configuration, listed under <a>WorkGroup$Configuration</a>. Each workgroup enables you to isolate queries for you or your group of users from other queries in the same account, to configure the query results location and the encryption configuration (known as workgroup settings), to enable sending query metrics to Amazon CloudWatch, and to establish per-query data usage control limits for all queries in a workgroup. The workgroup settings override is specified in <code>EnforceWorkGroupConfiguration</code> (true/false) in the <code>WorkGroupConfiguration</code>. See <a>WorkGroupConfiguration$EnforceWorkGroupConfiguration</a>.


# Interface Name

`WorkGroup`


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
  WorkGroup,
  WorkGroupState3Enum,
} from 'amazon-athenalib';

const workGroup: WorkGroup = {
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
  description: 'Description6',
  creationTime: '2016-03-13T12:52:32.123Z',
};
```



