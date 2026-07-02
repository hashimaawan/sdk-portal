# Slack Webhooks to Send Alerts To

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlNsYWNrJTI1MjBXZWJob29rcyUyNTIwdG8lMjUyMHNlbmQlMjUyMGFsZXJ0cyUyNTIwdG8

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`SlackWebhooksToSendAlertsTo`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `channel` | `?string` | Optional | - | getChannel(): ?string | setChannel(?string channel): void |
| `url` | `?string` | Optional | - | getUrl(): ?string | setUrl(?string url): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\SlackWebhooksToSendAlertsToBuilder;
use DigitalOceanApiLib\ApiHelper;

$slackWebhooksToSendAlertsTo = SlackWebhooksToSendAlertsToBuilder::init()
    ->channel('Channel Name')
    ->url('https://hooks.slack.com/services/T00000000/B00000000/XXXXXXXXXXXXXXXXXXXXXXXX')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



