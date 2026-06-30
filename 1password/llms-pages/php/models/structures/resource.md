# Resource

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/php/x-redirect/JTI0bSUyRlJlc291cmNl

*This model accepts additional fields of type array.*


# Class Name

`Resource`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `item` | [`?Item2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/php/models/structures/item-2.md) | Optional | - | getItem(): ?Item2 | setItem(?Item2 item): void |
| `itemVersion` | `?int` | Optional | - | getItemVersion(): ?int | setItemVersion(?int itemVersion): void |
| `type` | [`?string(Type)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/php/models/enumerations/type.md) | Optional | - | getType(): ?string | setType(?string type): void |
| `vault` | [`?Vault3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/php/models/structures/vault-3.md) | Optional | - | getVault(): ?Vault3 | setVault(?Vault3 vault): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use M1PasswordConnectLib\Models\Builders\Resource2Builder;
use M1PasswordConnectLib\Models\Builders\Item2Builder;
use M1PasswordConnectLib\ApiHelper;
use M1PasswordConnectLib\Models\Type;
use M1PasswordConnectLib\Models\Builders\Vault3Builder;

$resource = Resource2Builder::init()
    ->item(
        Item2Builder::init()
            ->id('id2')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->itemVersion(108)
    ->type(Type::ITEM)
    ->vault(
        Vault3Builder::init()
            ->id('id6')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



