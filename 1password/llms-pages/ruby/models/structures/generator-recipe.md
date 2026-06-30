# Generator Recipe

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/ruby/x-redirect/JTI0bSUyRkdlbmVyYXRvclJlY2lwZQ

The recipe is used in conjunction with the "generate" property to set the character set used to generate a new secure value

*This model accepts additional fields of type Object.*


# Class Name

`GeneratorRecipe`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `character_sets` | [`Array[CharacterSet]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/ruby/models/enumerations/character-set.md) | Optional | **Constraints**: *Unique Items Required* |
| `exclude_characters` | `String` | Optional | List of all characters that should be excluded from generated passwords. |
| `length` | `Integer` | Optional | Length of the generated value<br><br>**Default**: `32`<br><br>**Constraints**: `>= 1`, `<= 64` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
generator_recipe = GeneratorRecipe.new(
  character_sets: [
    CharacterSet::LETTERS,
    CharacterSet::SYMBOLS,
    CharacterSet::DIGITS
  ],
  exclude_characters: 'abc1',
  length: 32,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



