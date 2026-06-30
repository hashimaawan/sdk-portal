# Url

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/python/x-redirect/JTI0bSUyRlVybA

*This model accepts additional fields of type Any.*


# Class Name

`Url`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `href` | `str` | Required | - |
| `label` | `str` | Optional | - |
| `primary` | `bool` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from m1passwordconnect.models.url import Url

url = Url(
    href='href6',
    label='label4',
    primary=False,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



