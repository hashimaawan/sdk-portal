# Networks

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRk5ldHdvcmtz

The details of the network that are configured for the Droplet instance.  This is an object that contains keys for IPv4 and IPv6.  The value of each of these is an array that contains objects describing an individual IP resource allocated to the Droplet.  These will define attributes like the IP address, netmask, and gateway of the specific network depending on the type of network it is.

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Networks`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `v4` | [`?(V4[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/v4.md) | Optional | - | getV4(): ?array | setV4(?array v4): void |
| `v6` | [`?(V6[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/v6.md) | Optional | - | getV6(): ?array | setV6(?array v6): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\NetworksBuilder;
use DigitalOceanApiLib\Models\Builders\V4Builder;
use DigitalOceanApiLib\Models\Type10;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Models\Builders\V6Builder;
use DigitalOceanApiLib\Models\Type11;

$networks = NetworksBuilder::init()
    ->v4(
        [
            V4Builder::init()
                ->gateway('gateway2')
                ->ipAddress('ip_address2')
                ->netmask('netmask2')
                ->type(Type10::PUBLIC_)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            V4Builder::init()
                ->gateway('gateway2')
                ->ipAddress('ip_address2')
                ->netmask('netmask2')
                ->type(Type10::PUBLIC_)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            V4Builder::init()
                ->gateway('gateway2')
                ->ipAddress('ip_address2')
                ->netmask('netmask2')
                ->type(Type10::PUBLIC_)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->v6(
        [
            V6Builder::init()
                ->gateway('gateway4')
                ->ipAddress('ip_address4')
                ->netmask(106)
                ->type(Type11::PUBLIC_)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            V6Builder::init()
                ->gateway('gateway4')
                ->ipAddress('ip_address4')
                ->netmask(106)
                ->type(Type11::PUBLIC_)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



