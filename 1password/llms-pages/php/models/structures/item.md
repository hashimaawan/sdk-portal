# Item

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/php/x-redirect/JTI0bSUyRkl0ZW0

*This model accepts additional fields of type array.*


# Class Name

`Item`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `category` | [`string(Category)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/php/models/enumerations/category.md) | Required | - | getCategory(): string | setCategory(string category): void |
| `createdAt` | `?DateTime` | Optional, Read-only | - | getCreatedAt(): ?\DateTime | setCreatedAt(?\DateTime createdAt): void |
| `favorite` | `?bool` | Optional | **Default**: `false` | getFavorite(): ?bool | setFavorite(?bool favorite): void |
| `id` | `?string` | Optional | **Constraints**: *Pattern*: `^[\da-z]{26}$` | getId(): ?string | setId(?string id): void |
| `lastEditedBy` | `?string` | Optional, Read-only | - | getLastEditedBy(): ?string | setLastEditedBy(?string lastEditedBy): void |
| `state` | [`?string(State)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/php/models/enumerations/state.md) | Optional, Read-only | - | getState(): ?string | setState(?string state): void |
| `tags` | `?(string[])` | Optional | - | getTags(): ?array | setTags(?array tags): void |
| `title` | `?string` | Optional | - | getTitle(): ?string | setTitle(?string title): void |
| `updatedAt` | `?DateTime` | Optional, Read-only | - | getUpdatedAt(): ?\DateTime | setUpdatedAt(?\DateTime updatedAt): void |
| `urls` | [`?(Url[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/php/models/structures/url.md) | Optional | - | getUrls(): ?array | setUrls(?array urls): void |
| `vault` | [`Vault1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/php/models/structures/vault-1.md) | Required | - | getVault(): Vault1 | setVault(Vault1 vault): void |
| `version` | `?int` | Optional | - | getVersion(): ?int | setVersion(?int version): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use M1PasswordConnectLib\Models\Builders\ItemBuilder;
use M1PasswordConnectLib\Models\Category;
use M1PasswordConnectLib\Models\Builders\Vault1Builder;
use M1PasswordConnectLib\ApiHelper;
use M1PasswordConnectLib\Utils\DateTimeHelper;
use M1PasswordConnectLib\Models\State;
use M1PasswordConnectLib\Models\Builders\UrlBuilder;

$item = ItemBuilder::init(
    Category::SSH_KEY,
    Vault1Builder::init(
        'id6'
    )
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build()
)
    ->createdAt(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
    ->favorite(false)
    ->id('id2')
    ->lastEditedBy('lastEditedBy8')
    ->state(State::ARCHIVED)
    ->urls(
        [
            UrlBuilder::init(
                'https://example.com'
            )
                ->primary(true)
                ->build(),
            UrlBuilder::init(
                'https://example.org'
            )->build()
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



