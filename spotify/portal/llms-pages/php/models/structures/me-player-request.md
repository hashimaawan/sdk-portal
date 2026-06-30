# Me Player Request

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/php/x-redirect/JTI0bSUyRk1lJTI1MjBQbGF5ZXIlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type array.*


# Class Name

`MePlayerRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `deviceIds` | `string[]` | Required | A JSON array containing the ID of the device on which playback should be started/transferred.<br/>For example:`{device_ids:["74ASZWbe4lXaubB36ztrGX"]}`<br/>_**Note**: Although an array is accepted, only a single device_id is currently supported. Supplying more than one will return `400 Bad Request`_ | getDeviceIds(): array | setDeviceIds(array deviceIds): void |
| `play` | `?bool` | Optional | **true**: ensure playback happens on new device.<br/>**false** or not provided: keep the current playback state. | getPlay(): ?bool | setPlay(?bool play): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\MePlayerRequestBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\ApiHelper;

$mePlayerRequest = MePlayerRequestBuilder::init(
    [
        '74ASZWbe4lXaubB36ztrGX'
    ]
)
    ->play(false)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



