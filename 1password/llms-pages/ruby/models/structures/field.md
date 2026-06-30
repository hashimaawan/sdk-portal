# Field

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/ruby/x-redirect/JTI0bSUyRkZpZWxk

*This model accepts additional fields of type Object.*


# Class Name

`Field`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `entropy` | `Float` | Optional, Read-only | For fields with a purpose of `PASSWORD` this is the entropy of the value |
| `generate` | `TrueClass \| FalseClass` | Optional | If value is not present then a new value should be generated for this field<br><br>**Default**: `false` |
| `id` | `String` | Required | - |
| `label` | `String` | Optional | - |
| `purpose` | [`Purpose`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/ruby/models/enumerations/purpose.md) | Optional | Some item types, Login and Password, have fields used for autofill. This property indicates that purpose and is required for some item types. |
| `recipe` | [`GeneratorRecipe`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/ruby/models/structures/generator-recipe.md) | Optional | The recipe is used in conjunction with the "generate" property to set the character set used to generate a new secure value |
| `section` | [`Section`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/ruby/models/structures/section.md) | Optional | - |
| `type` | [`Type1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/ruby/models/enumerations/type-1.md) | Required | **Default**: `Type1::STRING` |
| `value` | `String` | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
field = Field.new(
  id: 'id6',
  type: Type1::STRING,
  entropy: 80.94,
  generate: false,
  label: 'label6',
  purpose: Purpose::NOTES,
  recipe: GeneratorRecipe.new(
    character_sets: [
      CharacterSet::LETTERS,
      CharacterSet::SYMBOLS,
      CharacterSet::DIGITS
    ],
    exclude_characters: 'excludeCharacters0',
    length: 64,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



