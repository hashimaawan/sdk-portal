# V2 Apps Components Logs Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBDb21wb25lbnRzJTI1MjBMb2dzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2AppsComponentsLogsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `historicUrls` | `?(string[])` | Optional | - | getHistoricUrls(): ?array | setHistoricUrls(?array historicUrls): void |
| `liveUrl` | `?string` | Optional | A URL of the real-time live logs. This URL may use either the `https://` or `wss://` protocols and will keep pushing live logs as they become available. | getLiveUrl(): ?string | setLiveUrl(?string liveUrl): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2AppsComponentsLogsResponseBuilder;
use DigitalOceanApiLib\ApiHelper;

$v2AppsComponentsLogsResponse = V2AppsComponentsLogsResponseBuilder::init()
    ->historicUrls(
        [
            'historic_urls9',
            'historic_urls0',
            'historic_urls1'
        ]
    )
    ->liveUrl('ws://logs/build')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



