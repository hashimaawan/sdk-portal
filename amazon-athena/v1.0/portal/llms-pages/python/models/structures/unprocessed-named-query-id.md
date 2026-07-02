# Unprocessed Named Query Id

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlVucHJvY2Vzc2VkTmFtZWRRdWVyeUlk

Information about a named query ID that could not be processed.

*This model accepts additional fields of type Any.*


# Class Name

`UnprocessedNamedQueryId`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `named_query_id` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |
| `error_code` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `error_message` | `str` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.unprocessed_named_query_id import UnprocessedNamedQueryId

unprocessed_named_query_id = UnprocessedNamedQueryId(
    named_query_id='NamedQueryId8',
    error_code='ErrorCode6',
    error_message='ErrorMessage6',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



