# Full Item

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/python/x-redirect/JTI0bSUyRkZ1bGxJdGVt

*This model accepts additional fields of type Any.*


# Class Name

`FullItem`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `category` | [`Category`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/python/models/enumerations/category.md) | Required | - |
| `created_at` | `datetime` | Optional, Read-only | - |
| `favorite` | `bool` | Optional | **Default**: `False` |
| `id` | `str` | Optional | **Constraints**: *Pattern*: `^[\da-z]{26}$` |
| `last_edited_by` | `str` | Optional, Read-only | - |
| `state` | [`State`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/python/models/enumerations/state.md) | Optional, Read-only | - |
| `tags` | `List[str]` | Optional | - |
| `title` | `str` | Optional | - |
| `updated_at` | `datetime` | Optional, Read-only | - |
| `urls` | [`List[Url]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/python/models/structures/url.md) | Optional | - |
| `vault` | [`Vault1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/python/models/structures/vault-1.md) | Required | - |
| `version` | `int` | Optional | - |
| `fields` | [`List[Field]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/python/models/structures/field.md) | Optional | - |
| `files` | [`List[File]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/python/models/structures/file.md) | Optional | - |
| `sections` | [`List[Section2]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/python/models/structures/section-2.md) | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from m1passwordconnect.models.category import Category
from m1passwordconnect.models.full_item import FullItem
from m1passwordconnect.models.state import State
from m1passwordconnect.models.url import Url
from m1passwordconnect.models.vault_1 import Vault1

full_item = FullItem(
    category=Category.SOCIAL_SECURITY_NUMBER,
    vault=Vault1(
        id='id6',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    favorite=False,
    id='id4',
    last_edited_by='lastEditedBy0',
    state=State.ARCHIVED,
    urls=[
        Url(
            href='https://example.com',
            primary=True
        ),
        Url(
            href='https://example.org'
        )
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



