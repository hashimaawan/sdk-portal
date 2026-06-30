# Field

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/python/x-redirect/JTI0bSUyRkZpZWxk

*This model accepts additional fields of type Any.*


# Class Name

`Field`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `entropy` | `float` | Optional, Read-only | For fields with a purpose of `PASSWORD` this is the entropy of the value |
| `generate` | `bool` | Optional | If value is not present then a new value should be generated for this field<br><br>**Default**: `False` |
| `id` | `str` | Required | - |
| `label` | `str` | Optional | - |
| `purpose` | [`Purpose`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/python/models/enumerations/purpose.md) | Optional | Some item types, Login and Password, have fields used for autofill. This property indicates that purpose and is required for some item types. |
| `recipe` | [`GeneratorRecipe`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/python/models/structures/generator-recipe.md) | Optional | The recipe is used in conjunction with the "generate" property to set the character set used to generate a new secure value |
| `section` | [`Section`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/python/models/structures/section.md) | Optional | - |
| `mtype` | [`Type1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/python/models/enumerations/type-1.md) | Required | **Default**: `"STRING"` |
| `value` | `str` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from m1passwordconnect.models.character_set import CharacterSet
from m1passwordconnect.models.field import Field
from m1passwordconnect.models.generator_recipe import GeneratorRecipe
from m1passwordconnect.models.purpose import Purpose
from m1passwordconnect.models.type_1 import Type1

field = Field(
    id='id6',
    mtype=Type1.STRING,
    entropy=80.94,
    generate=False,
    label='label6',
    purpose=Purpose.NOTES,
    recipe=GeneratorRecipe(
        character_sets=[
            CharacterSet.LETTERS,
            CharacterSet.SYMBOLS,
            CharacterSet.DIGITS
        ],
        exclude_characters='excludeCharacters0',
        length=64,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



