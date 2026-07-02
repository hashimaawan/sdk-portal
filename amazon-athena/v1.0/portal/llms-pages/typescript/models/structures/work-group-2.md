# Work Group 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRldvcmtHcm91cDI

*This model accepts additional fields of type unknown.*


# Interface Name

`WorkGroup2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `string` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `state` | [`WorkGroupState3 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/enumerations/work-group-state-3.md) | Optional | - |
| `configuration` | [`MConfiguration \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/configuration.md) | Optional | - |
| `description` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `1024` |
| `creationTime` | `string \| undefined` | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  EncryptionOption1,
  S3AclOption1,
  WorkGroup2,
  WorkGroupState3,
} from 'amazon-athenalib';

const workGroup2: WorkGroup2 = {
  name: 'Name0',
  state: WorkGroupState3.Enabled,
  configuration: {
    resultConfiguration: {
      outputLocation: 'OutputLocation0',
      encryptionConfiguration: {
        encryptionOption: EncryptionOption1.SseS3,
        kmsKey: 'KmsKey6',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      expectedBucketOwner: 'ExpectedBucketOwner0',
      aclConfiguration: {
        s3AclOption: S3AclOption1.BucketOwnerFullControl,
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    enforceWorkGroupConfiguration: false,
    publishCloudWatchMetricsEnabled: false,
    bytesScannedCutoffPerQuery: 10000000,
    requesterPaysEnabled: false,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  description: 'Description6',
  creationTime: '2016-03-13T12:52:32.123Z',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



