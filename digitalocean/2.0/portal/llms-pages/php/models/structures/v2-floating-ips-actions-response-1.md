# V2 Floating Ips Actions Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBGbG9hdGluZyUyNTIwSXBzJTI1MjBBY3Rpb25zJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2FloatingIpsActionsResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `action` | [`?Action2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/action-2.md) | Optional | - | getAction(): ?Action2 | setAction(?Action2 action): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2FloatingIpsActionsResponse1Builder;
use DigitalOceanApiLib\Models\Builders\Action2Builder;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\Models\Builders\RegionBuilder;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Models\Status1;

$v2FloatingIpsActionsResponse1 = V2FloatingIpsActionsResponse1Builder::init()
    ->action(
        Action2Builder::init()
            ->completedAt(DateTimeHelper::fromRfc3339DateTime('2015-11-12T17:51:14Z'))
            ->id(72531856)
            ->region(
                RegionBuilder::init(
                    true,
                    [
                        'private_networking',
                        'backups',
                        'ipv6',
                        'metadata'
                    ],
                    'New York 3',
                    [
                        's-1vcpu-1gb',
                        's-1vcpu-2gb',
                        's-1vcpu-3gb',
                        's-2vcpu-2gb',
                        's-3vcpu-1gb',
                        's-2vcpu-4gb',
                        's-4vcpu-8gb',
                        's-6vcpu-16gb',
                        's-8vcpu-32gb',
                        's-12vcpu-48gb',
                        's-16vcpu-64gb',
                        's-20vcpu-96gb',
                        's-24vcpu-128gb',
                        's-32vcpu-192gb'
                    ],
                    'nyc3'
                )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            )
            ->regionSlug('nyc3')
            ->resourceId(758604968)
            ->resourceType('floating_ip')
            ->startedAt(DateTimeHelper::fromRfc3339DateTime('2015-11-12T17:51:03Z'))
            ->status(Status1::COMPLETED)
            ->type('assign_ip')
            ->projectId('746c6152-2fa2-11ed-92d3-27aaa54e4988')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



