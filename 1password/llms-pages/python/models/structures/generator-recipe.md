# Generator Recipe

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/python/x-redirect/JTI0bSUyRkdlbmVyYXRvclJlY2lwZQ

The recipe is used in conjunction with the "generate" property to set the character set used to generate a new secure value

*This model accepts additional fields of type Any.*


# Class Name

`GeneratorRecipe`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `character_sets` | [`List[CharacterSet]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/python/models/enumerations/character-set.md) | Optional | **Constraints**: *Unique Items Required* |
| `exclude_characters` | `str` | Optional | List of all characters that should be excluded from generated passwords. |
| `length` | `int` | Optional | Length of the generated value<br><br>**Default**: `32`<br><br>**Constraints**: `>= 1`, `<= 64` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from m1passwordconnect.models.character_set import CharacterSet
from m1passwordconnect.models.generator_recipe import GeneratorRecipe

generator_recipe = GeneratorRecipe(
    character_sets=[
        CharacterSet.LETTERS,
        CharacterSet.SYMBOLS,
        CharacterSet.DIGITS
    ],
    exclude_characters='abc1',
    length=32,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



