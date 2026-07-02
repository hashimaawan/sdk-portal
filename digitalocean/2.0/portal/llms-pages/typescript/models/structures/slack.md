# Slack

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlNsYWNr

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Slack`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `channel` | `string` | Required | Slack channel to notify of an alert trigger. |
| `url` | `string` | Required | Slack Webhook URL. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Slack } from 'digitalocean-apilib';

const slack: Slack = {
  channel: 'Production Alerts',
  url: 'https://hooks.slack.com/services/T1234567/AAAAAAAA/ZZZZZZ',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



