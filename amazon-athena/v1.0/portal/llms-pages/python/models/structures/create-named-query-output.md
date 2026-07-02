# Create Named Query Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkNyZWF0ZU5hbWVkUXVlcnlPdXRwdXQ

*This model accepts additional fields of type Any.*


# Class Name

`CreateNamedQueryOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `named_query_id` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.create_named_query_output import CreateNamedQueryOutput

create_named_query_output = CreateNamedQueryOutput(
    named_query_id='NamedQueryId4',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



