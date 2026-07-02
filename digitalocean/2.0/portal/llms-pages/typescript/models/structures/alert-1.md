# Alert 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkFsZXJ0MQ

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Alert1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `componentName` | `string \| undefined` | Optional | - |
| `emails` | `string[] \| undefined` | Optional | - |
| `id` | `string \| undefined` | Optional, Read-only | - |
| `phase` | [`Phase1 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/phase-1.md) | Optional | **Default**: `Phase1.Unknown` |
| `progress` | [`Progress2 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/progress-2.md) | Optional | - |
| `slackWebhooks` | [`SlackWebhooksToSendAlertsTo[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/slack-webhooks-to-send-alerts-to.md) | Optional | - |
| `spec` | [`Alert \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/alert.md) | Optional | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Alert1, Phase1, Status2 } from 'digitalocean-apilib';

const alert1: Alert1 = {
  componentName: 'backend',
  emails: [
    'sammy@digitalocean.com'
  ],
  id: '4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf',
  phase: Phase1.Active,
  progress: {
    steps: [
      {
        endedAt: '2016-03-13T12:52:32.123Z',
        name: 'name2',
        reason: {
          code: 'code2',
          message: 'message4',
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        startedAt: '2016-03-13T12:52:32.123Z',
        status: Status2.Success,
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      {
        endedAt: '2016-03-13T12:52:32.123Z',
        name: 'name2',
        reason: {
          code: 'code2',
          message: 'message4',
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        startedAt: '2016-03-13T12:52:32.123Z',
        status: Status2.Success,
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      {
        endedAt: '2016-03-13T12:52:32.123Z',
        name: 'name2',
        reason: {
          code: 'code2',
          message: 'message4',
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        startedAt: '2016-03-13T12:52:32.123Z',
        status: Status2.Success,
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      }
    ],
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



