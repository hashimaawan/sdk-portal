# Followers Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/php/x-redirect/JTI0bSUyRkZvbGxvd2Vyc09iamVjdA

*This model accepts additional fields of type array.*


# Class Name

`FollowersObject`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `href` | `?string` | Optional | This will always be set to null, as the Web API does not support it at the moment. | getHref(): ?string | setHref(?string href): void |
| `total` | `?int` | Optional | The total number of followers. | getTotal(): ?int | setTotal(?int total): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\FollowersObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\ApiHelper;

$followersObject = FollowersObjectBuilder::init()
    ->href('href2')
    ->total(62)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



