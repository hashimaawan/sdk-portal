# Generator Recipe

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/php/x-redirect/JTI0bSUyRkdlbmVyYXRvclJlY2lwZQ

The recipe is used in conjunction with the "generate" property to set the character set used to generate a new secure value

*This model accepts additional fields of type array.*


# Class Name

`GeneratorRecipe`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `characterSets` | [`?(string(CharacterSet)[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/php/models/enumerations/character-set.md) | Optional | **Constraints**: *Unique Items Required* | getCharacterSets(): ?array | setCharacterSets(?array characterSets): void |
| `excludeCharacters` | `?string` | Optional | List of all characters that should be excluded from generated passwords. | getExcludeCharacters(): ?string | setExcludeCharacters(?string excludeCharacters): void |
| `length` | `?int` | Optional | Length of the generated value<br><br>**Default**: `32`<br><br>**Constraints**: `>= 1`, `<= 64` | getLength(): ?int | setLength(?int length): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use M1PasswordConnectLib\Models\Builders\GeneratorRecipeBuilder;
use M1PasswordConnectLib\Models\CharacterSet;
use M1PasswordConnectLib\ApiHelper;

$generatorRecipe = GeneratorRecipeBuilder::init()
    ->characterSets(
        [
            CharacterSet::LETTERS,
            CharacterSet::DIGITS,
            CharacterSet::SYMBOLS
        ]
    )
    ->excludeCharacters('abc1')
    ->length(32)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



