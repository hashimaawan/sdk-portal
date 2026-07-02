# V2 Firewalls Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBGaXJld2FsbHMlMjUyMFJlc3BvbnNlMQ

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2FirewallsResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `firewall` | [`?Firewall`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/firewall.md) | Optional | - | getFirewall(): ?Firewall | setFirewall(?Firewall firewall): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2FirewallsResponse1Builder;
use DigitalOceanApiLib\Models\Builders\FirewallBuilder;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\Models\Builders\PendingChangeBuilder;
use DigitalOceanApiLib\ApiHelper;

$v2FirewallsResponse1 = V2FirewallsResponse1Builder::init()
    ->firewall(
        FirewallBuilder::init()
            ->createdAt(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
            ->dropletIds(
                [
                    67
                ]
            )
            ->id('id6')
            ->name('name6')
            ->pendingChanges(
                [
                    null,
                    PendingChangeBuilder::init()->build(),
                    PendingChangeBuilder::init()->build()
                ]
            )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



