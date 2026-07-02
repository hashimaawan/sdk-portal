# V2 Apps Alerts Destinations Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBBbGVydHMlMjUyMERlc3RpbmF0aW9ucyUyNTIwUmVxdWVzdA

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2AppsAlertsDestinationsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `emails` | `string[] \| undefined` | Optional | - |
| `slackWebhooks` | [`SlackWebhooksToSendAlertsTo[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/slack-webhooks-to-send-alerts-to.md) | Optional | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { V2AppsAlertsDestinationsRequest } from 'digitalocean-apilib';

const v2AppsAlertsDestinationsRequest: V2AppsAlertsDestinationsRequest = {
  emails: [
    'sammy@digitalocean.com'
  ],
  slackWebhooks: [
    {
      channel: 'channel8',
      url: 'url0',
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



