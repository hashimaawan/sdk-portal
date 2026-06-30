# File

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/php/x-redirect/JTI0bSUyRkZpbGU

*This model accepts additional fields of type array.*


# Class Name

`File`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `content` | `?string` | Optional | Base64-encoded contents of the file. Only set if size <= OP_MAX_INLINE_FILE_SIZE_KB kb and `inline_files` is set to `true`. | getContent(): ?string | setContent(?string content): void |
| `contentPath` | `?string` | Optional, Read-only | Path of the Connect API that can be used to download the contents of this file. | getContentPath(): ?string | setContentPath(?string contentPath): void |
| `id` | `?string` | Optional | ID of the file | getId(): ?string | setId(?string id): void |
| `name` | `?string` | Optional | Name of the file | getName(): ?string | setName(?string name): void |
| `section` | [`?Section1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/php/models/structures/section-1.md) | Optional | For files that are in a section, this field describes the section. | getSection(): ?Section1 | setSection(?Section1 section): void |
| `size` | `?int` | Optional | Size in bytes of the file | getSize(): ?int | setSize(?int size): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use M1PasswordConnectLib\Models\Builders\FileBuilder;
use M1PasswordConnectLib\Models\Builders\Section1Builder;
use M1PasswordConnectLib\ApiHelper;

$file = FileBuilder::init()
    ->content('VGhlIGZ1dHVyZSBiZWxvbmdzIHRvIHRoZSBjdXJpb3VzLgo=')
    ->contentPath('v1/vaults/ionaiwtdvgclrixbt6ztpqcxnq/items/p7eflcy7f5mk7vg6zrzf5rjjyu/files/6r65pjq33banznomn7q22sj44e/content')
    ->id('6r65pjq33banznomn7q22sj44e')
    ->name('foo.txt')
    ->section(
        Section1Builder::init()
            ->id('id6')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->size(35)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



