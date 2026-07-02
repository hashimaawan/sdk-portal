# Slack Webhooks to Send Alerts To

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlNsYWNrJTI1MjBXZWJob29rcyUyNTIwdG8lMjUyMHNlbmQlMjUyMGFsZXJ0cyUyNTIwdG8

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`SlackWebhooksToSendAlertsTo`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `channel` | `string \| undefined` | Optional | - |
| `url` | `string \| undefined` | Optional | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { SlackWebhooksToSendAlertsTo } from 'digitalocean-apilib';

const slackWebhooksToSendAlertsTo: SlackWebhooksToSendAlertsTo = {
  channel: 'Channel Name',
  url: 'https://hooks.slack.com/services/T00000000/B00000000/XXXXXXXXXXXXXXXXXXXXXXXX',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



