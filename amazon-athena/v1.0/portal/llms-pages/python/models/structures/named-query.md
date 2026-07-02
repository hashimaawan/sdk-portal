# Named Query

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRk5hbWVkUXVlcnk

A query, where <code>QueryString</code> contains the SQL statements that make up the query.

*This model accepts additional fields of type Any.*


# Class Name

`NamedQuery`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `str` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `description` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `database` | `str` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` |
| `query_string` | `str` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `262144` |
| `named_query_id` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |
| `work_group` | `str` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.named_query import NamedQuery

named_query = NamedQuery(
    name='Name4',
    database='Database2',
    query_string='QueryString6',
    description='Description8',
    named_query_id='NamedQueryId8',
    work_group='WorkGroup6',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



