# Markets

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/python/x-redirect/JTI0bSUyRk1hcmtldHM

*This model accepts additional fields of type Any.*


# Class Name

`Markets`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `markets` | `List[str]` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from spotifywebapiwithfixesandimprovementsfromsonallux.models.markets import Markets

markets = Markets(
    markets=[
        'CA',
        'BR',
        'IT'
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



