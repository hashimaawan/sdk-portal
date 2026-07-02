# Create Work Group Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkNyZWF0ZVdvcmtHcm91cElucHV0

*This model accepts additional fields of type unknown.*


# Interface Name

`CreateWorkGroupInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `string` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `configuration` | [`MConfiguration \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/configuration.md) | Optional | - |
| `description` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `1024` |
| `tags` | [`Tag[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/tag.md) | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  CreateWorkGroupInput,
  EncryptionOption1,
  S3AclOption1,
} from 'amazon-athenalib';

const createWorkGroupInput: CreateWorkGroupInput = {
  name: 'Name6',
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
  description: 'Description0',
  tags: [
    {
      key: 'Key0',
      value: 'Value6',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      key: 'Key0',
      value: 'Value6',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



