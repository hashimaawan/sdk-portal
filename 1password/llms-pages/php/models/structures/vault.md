# Vault

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/php/x-redirect/JTI0bSUyRlZhdWx0

*This model accepts additional fields of type array.*


# Class Name

`Vault`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `attributeVersion` | `?int` | Optional | The vault version | getAttributeVersion(): ?int | setAttributeVersion(?int attributeVersion): void |
| `contentVersion` | `?int` | Optional | The version of the vault contents | getContentVersion(): ?int | setContentVersion(?int contentVersion): void |
| `createdAt` | `?DateTime` | Optional, Read-only | - | getCreatedAt(): ?\DateTime | setCreatedAt(?\DateTime createdAt): void |
| `description` | `?string` | Optional | - | getDescription(): ?string | setDescription(?string description): void |
| `id` | `?string` | Optional | **Constraints**: *Pattern*: `^[\da-z]{26}$` | getId(): ?string | setId(?string id): void |
| `items` | `?int` | Optional | Number of active items in the vault | getItems(): ?int | setItems(?int items): void |
| `name` | `?string` | Optional | - | getName(): ?string | setName(?string name): void |
| `type` | [`?string(Type2)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/php/models/enumerations/type-2.md) | Optional | - | getType(): ?string | setType(?string type): void |
| `updatedAt` | `?DateTime` | Optional, Read-only | - | getUpdatedAt(): ?\DateTime | setUpdatedAt(?\DateTime updatedAt): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use M1PasswordConnectLib\Models\Builders\VaultBuilder;
use M1PasswordConnectLib\Utils\DateTimeHelper;
use M1PasswordConnectLib\ApiHelper;

$vault = VaultBuilder::init()
    ->attributeVersion(108)
    ->contentVersion(228)
    ->createdAt(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
    ->description('description6')
    ->id('id6')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



