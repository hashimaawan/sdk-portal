# Many Devices

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/php/x-redirect/JTI0bSUyRk1hbnlEZXZpY2Vz

*This model accepts additional fields of type array.*


# Class Name

`ManyDevices`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `devices` | [`DeviceObject[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/php/models/structures/device-object.md) | Required | - | getDevices(): array | setDevices(array devices): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\ManyDevicesBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\DeviceObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\ApiHelper;

$manyDevices = ManyDevicesBuilder::init(
    [
        DeviceObjectBuilder::init()
            ->id('id4')
            ->isActive(false)
            ->isPrivateSession(false)
            ->isRestricted(false)
            ->name('Kitchen speaker')
            ->type('computer')
            ->volumePercent(59)
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    ]
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



