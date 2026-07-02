# Sticky Sessions

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlN0aWNreVNlc3Npb25z

An object specifying sticky sessions settings for the load balancer.

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`StickySessions`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `cookieName` | `?string` | Optional | The name of the cookie sent to the client. This attribute is only returned when using `cookies` for the sticky sessions type. | getCookieName(): ?string | setCookieName(?string cookieName): void |
| `cookieTtlSeconds` | `?int` | Optional | The number of seconds until the cookie set by the load balancer expires. This attribute is only returned when using `cookies` for the sticky sessions type. | getCookieTtlSeconds(): ?int | setCookieTtlSeconds(?int cookieTtlSeconds): void |
| `type` | [`?string(Type16)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/type-16.md) | Optional | An attribute indicating how and if requests from a client will be persistently served by the same backend Droplet. The possible values are `cookies` or `none`.<br><br>**Default**: `Type16::NONE` | getType(): ?string | setType(?string type): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\StickySessionsBuilder;
use DigitalOceanApiLib\Models\Type16;
use DigitalOceanApiLib\ApiHelper;

$stickySessions = StickySessionsBuilder::init()
    ->cookieName('DO-LB')
    ->cookieTtlSeconds(300)
    ->type(Type16::COOKIES)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



