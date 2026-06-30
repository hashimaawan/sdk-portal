# File

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/python/x-redirect/JTI0bSUyRkZpbGU

*This model accepts additional fields of type Any.*


# Class Name

`File`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `content` | `str` | Optional | Base64-encoded contents of the file. Only set if size <= OP_MAX_INLINE_FILE_SIZE_KB kb and `inline_files` is set to `true`. |
| `content_path` | `str` | Optional, Read-only | Path of the Connect API that can be used to download the contents of this file. |
| `id` | `str` | Optional | ID of the file |
| `name` | `str` | Optional | Name of the file |
| `section` | [`Section1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/python/models/structures/section-1.md) | Optional | For files that are in a section, this field describes the section. |
| `size` | `int` | Optional | Size in bytes of the file |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from m1passwordconnect.models.file import File
from m1passwordconnect.models.section_1 import Section1

file = File(
    content='VGhlIGZ1dHVyZSBiZWxvbmdzIHRvIHRoZSBjdXJpb3VzLgo=',
    content_path='v1/vaults/ionaiwtdvgclrixbt6ztpqcxnq/items/p7eflcy7f5mk7vg6zrzf5rjjyu/files/6r65pjq33banznomn7q22sj44e/content',
    id='6r65pjq33banznomn7q22sj44e',
    name='foo.txt',
    section=Section1(
        id='id6',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    size=35,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



