# Explicit Content Settings Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/python/x-redirect/JTI0bSUyRkV4cGxpY2l0Q29udGVudFNldHRpbmdzT2JqZWN0

*This model accepts additional fields of type Any.*


# Class Name

`ExplicitContentSettingsObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `filter_enabled` | `bool` | Optional | When `true`, indicates that explicit content should not be played. |
| `filter_locked` | `bool` | Optional | When `true`, indicates that the explicit content setting is locked and can't be changed by the user. |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from spotifywebapiwithfixesandimprovementsfromsonallux.models.explicit_content_settings_object import ExplicitContentSettingsObject

explicit_content_settings_object = ExplicitContentSettingsObject(
    filter_enabled=False,
    filter_locked=False,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



