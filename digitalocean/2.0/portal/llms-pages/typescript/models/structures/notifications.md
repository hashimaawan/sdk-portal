# Notifications

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRk5vdGlmaWNhdGlvbnM

The notification settings for a trigger alert.

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Notifications`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `email` | `string[]` | Required | An email to notify on an alert trigger. |
| `slack` | [`Slack[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/slack.md) | Required | Slack integration details. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Notifications } from 'digitalocean-apilib';

const notifications: Notifications = {
  email: [
    'bob@example.com'
  ],
  slack: [
    {
      channel: 'Production Alerts',
      url: 'https://hooks.slack.com/services/T1234567/AAAAAAAA/ZZZZZZ',
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



