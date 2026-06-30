# Copyright Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/python/x-redirect/JTI0bSUyRkNvcHlyaWdodE9iamVjdA

*This model accepts additional fields of type Any.*


# Class Name

`CopyrightObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `text` | `str` | Optional | The copyright text for this content. |
| `mtype` | `str` | Optional | The type of copyright: `C` = the copyright, `P` = the sound recording (performance) copyright. |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from spotifywebapiwithfixesandimprovementsfromsonallux.models.copyright_object import CopyrightObject

copyright_object = CopyrightObject(
    text='text6',
    mtype='type6',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



