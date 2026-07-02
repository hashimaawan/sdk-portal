# Create Work Group Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkNyZWF0ZVdvcmtHcm91cElucHV0


# Interface Name

`CreateWorkGroupInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `string` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `configuration` | [`MConfiguration \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/configuration.md) | Optional | - |
| `description` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `1024` |
| `tags` | [`Tag[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/tag.md) | Optional | - |


# Example

```ts
import {
  CreateWorkGroupInput,
  EncryptionOption1Enum,
  S3AclOption1Enum,
} from 'amazon-athenalib';

const createWorkGroupInput: CreateWorkGroupInput = {
  name: 'Name6',
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
  description: 'Description0',
  tags: [
    {
      key: 'Key0',
      value: 'Value6',
    },
    {
      key: 'Key0',
      value: 'Value6',
    }
  ],
};
```



