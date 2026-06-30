# Actor

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/php/x-redirect/JTI0bSUyRkFjdG9y

*This model accepts additional fields of type array.*


# Class Name

`Actor`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `account` | `?string` | Optional | - | getAccount(): ?string | setAccount(?string account): void |
| `id` | `?string` | Optional | - | getId(): ?string | setId(?string id): void |
| `jti` | `?string` | Optional | - | getJti(): ?string | setJti(?string jti): void |
| `requestIp` | `?string` | Optional | - | getRequestIp(): ?string | setRequestIp(?string requestIp): void |
| `userAgent` | `?string` | Optional | - | getUserAgent(): ?string | setUserAgent(?string userAgent): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use M1PasswordConnectLib\Models\Builders\ActorBuilder;
use M1PasswordConnectLib\ApiHelper;

$actor = ActorBuilder::init()
    ->account('account0')
    ->id('0000193c-0000-0000-0000-000000000000')
    ->jti('jti2')
    ->requestIp('requestIp4')
    ->userAgent('userAgent6')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



