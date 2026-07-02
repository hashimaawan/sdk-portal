# V2 Apps Alerts Destinations Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBBbGVydHMlMjUyMERlc3RpbmF0aW9ucyUyNTIwUmVxdWVzdA

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2AppsAlertsDestinationsRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `emails` | `?(string[])` | Optional | - | getEmails(): ?array | setEmails(?array emails): void |
| `slackWebhooks` | [`?(SlackWebhooksToSendAlertsTo[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/slack-webhooks-to-send-alerts-to.md) | Optional | - | getSlackWebhooks(): ?array | setSlackWebhooks(?array slackWebhooks): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2AppsAlertsDestinationsRequestBuilder;
use DigitalOceanApiLib\Models\Builders\SlackWebhooksToSendAlertsToBuilder;
use DigitalOceanApiLib\ApiHelper;

$v2AppsAlertsDestinationsRequest = V2AppsAlertsDestinationsRequestBuilder::init()
    ->emails(
        [
            'sammy@digitalocean.com'
        ]
    )
    ->slackWebhooks(
        [
            SlackWebhooksToSendAlertsToBuilder::init()
                ->channel('channel8')
                ->url('url0')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



