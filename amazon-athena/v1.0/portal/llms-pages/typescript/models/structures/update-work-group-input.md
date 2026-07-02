# Update Work Group Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlVwZGF0ZVdvcmtHcm91cElucHV0

*This model accepts additional fields of type unknown.*


# Interface Name

`UpdateWorkGroupInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `workGroup` | `string` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `description` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `1024` |
| `configurationUpdates` | [`ConfigurationUpdates \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/configuration-updates.md) | Optional | - |
| `state` | [`WorkGroupState2 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/enumerations/work-group-state-2.md) | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  EncryptionOption1,
  UpdateWorkGroupInput,
  WorkGroupState2,
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
        encryptionOption: EncryptionOption1.SseS3,
        kmsKey: 'KmsKey6',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      removeEncryptionConfiguration: false,
      expectedBucketOwner: 'ExpectedBucketOwner0',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    publishCloudWatchMetricsEnabled: false,
    bytesScannedCutoffPerQuery: 10000000,
    removeBytesScannedCutoffPerQuery: false,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  state: WorkGroupState2.Enabled,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



