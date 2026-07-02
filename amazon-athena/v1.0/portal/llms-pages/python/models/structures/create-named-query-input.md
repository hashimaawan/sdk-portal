# Create Named Query Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkNyZWF0ZU5hbWVkUXVlcnlJbnB1dA

*This model accepts additional fields of type Any.*


# Class Name

`CreateNamedQueryInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `str` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `description` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `database` | `str` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` |
| `query_string` | `str` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `262144` |
| `client_request_token` | `str` | Optional | **Constraints**: *Minimum Length*: `32`, *Maximum Length*: `128` |
| `work_group` | `str` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.create_named_query_input import CreateNamedQueryInput

create_named_query_input = CreateNamedQueryInput(
    name='Name0',
    database='Database8',
    query_string='QueryString2',
    description='Description6',
    client_request_token='ClientRequestToken4',
    work_group='WorkGroup2',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



