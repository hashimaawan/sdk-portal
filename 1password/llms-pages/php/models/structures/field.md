# Field

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/php/x-redirect/JTI0bSUyRkZpZWxk

*This model accepts additional fields of type array.*


# Class Name

`Field`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `entropy` | `?float` | Optional, Read-only | For fields with a purpose of `PASSWORD` this is the entropy of the value | getEntropy(): ?float | setEntropy(?float entropy): void |
| `generate` | `?bool` | Optional | If value is not present then a new value should be generated for this field<br><br>**Default**: `false` | getGenerate(): ?bool | setGenerate(?bool generate): void |
| `id` | `string` | Required | - | getId(): string | setId(string id): void |
| `label` | `?string` | Optional | - | getLabel(): ?string | setLabel(?string label): void |
| `purpose` | [`?string(Purpose)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/php/models/enumerations/purpose.md) | Optional | Some item types, Login and Password, have fields used for autofill. This property indicates that purpose and is required for some item types. | getPurpose(): ?string | setPurpose(?string purpose): void |
| `recipe` | [`?GeneratorRecipe`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/php/models/structures/generator-recipe.md) | Optional | The recipe is used in conjunction with the "generate" property to set the character set used to generate a new secure value | getRecipe(): ?GeneratorRecipe | setRecipe(?GeneratorRecipe recipe): void |
| `section` | [`?Section`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/php/models/structures/section.md) | Optional | - | getSection(): ?Section | setSection(?Section section): void |
| `type` | [`string(Type1)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/php/models/enumerations/type-1.md) | Required | **Default**: `Type1::STRING` | getType(): string | setType(string type): void |
| `value` | `?string` | Optional | - | getValue(): ?string | setValue(?string value): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use M1PasswordConnectLib\Models\Builders\FieldBuilder;
use M1PasswordConnectLib\Models\Type1;
use M1PasswordConnectLib\Models\Purpose;
use M1PasswordConnectLib\Models\Builders\GeneratorRecipeBuilder;
use M1PasswordConnectLib\Models\CharacterSet;
use M1PasswordConnectLib\ApiHelper;

$field = FieldBuilder::init(
    'id6',
    Type1::STRING
)
    ->entropy(80.94)
    ->generate(false)
    ->label('label6')
    ->purpose(Purpose::NOTES)
    ->recipe(
        GeneratorRecipeBuilder::init()
            ->characterSets(
                [
                    CharacterSet::LETTERS,
                    CharacterSet::SYMBOLS,
                    CharacterSet::DIGITS
                ]
            )
            ->excludeCharacters('excludeCharacters0')
            ->length(64)
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



