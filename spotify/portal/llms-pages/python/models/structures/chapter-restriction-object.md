# Chapter Restriction Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/python/x-redirect/JTI0bSUyRkNoYXB0ZXJSZXN0cmljdGlvbk9iamVjdA

*This model accepts additional fields of type Any.*


# Class Name

`ChapterRestrictionObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `reason` | `str` | Optional | The reason for the restriction. Supported values:<br><br>- `market` - The content item is not available in the given market.<br>- `product` - The content item is not available for the user's subscription type.<br>- `explicit` - The content item is explicit and the user's account is set to not play explicit content.<br>- `payment_required` - Payment is required to play the content item.<br><br>Additional reasons may be added in the future.<br>**Note**: If you use this field, make sure that your application safely handles unknown values. |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from spotifywebapiwithfixesandimprovementsfromsonallux.models.chapter_restriction_object import ChapterRestrictionObject

chapter_restriction_object = ChapterRestrictionObject(
    reason='reason8',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



