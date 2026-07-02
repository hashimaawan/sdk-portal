# Get Work Group Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkdldFdvcmtHcm91cE91dHB1dA

*This model accepts additional fields of type unknown.*


# Interface Name

`GetWorkGroupOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `workGroup` | [`WorkGroup2 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/work-group-2.md) | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  EncryptionOption1,
  GetWorkGroupOutput,
  S3AclOption1,
  WorkGroupState3,
} from 'amazon-athenalib';

const getWorkGroupOutput: GetWorkGroupOutput = {
  workGroup: {
    name: 'Name2',
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
    description: 'Description4',
    creationTime: '2016-03-13T12:52:32.123Z',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



