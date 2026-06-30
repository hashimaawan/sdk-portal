# External Id Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/python/x-redirect/JTI0bSUyRkV4dGVybmFsSWRPYmplY3Q

*This model accepts additional fields of type Any.*


# Class Name

`ExternalIdObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `isrc` | `str` | Optional | [International Standard Recording Code](http://en.wikipedia.org/wiki/International_Standard_Recording_Code) |
| `ean` | `str` | Optional | [International Article Number](http://en.wikipedia.org/wiki/International_Article_Number_%28EAN%29) |
| `upc` | `str` | Optional | [Universal Product Code](http://en.wikipedia.org/wiki/Universal_Product_Code) |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from spotifywebapiwithfixesandimprovementsfromsonallux.models.external_id_object import ExternalIdObject

external_id_object = ExternalIdObject(
    isrc='isrc8',
    ean='ean8',
    upc='upc2',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



