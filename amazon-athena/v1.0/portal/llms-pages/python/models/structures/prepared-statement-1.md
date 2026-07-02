# Prepared Statement 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlByZXBhcmVkU3RhdGVtZW50MQ


# Class Name

`PreparedStatement1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `statement_name` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256`, *Pattern*: `[a-zA-Z_][a-zA-Z0-9_@:]{1,256}` |
| `query_statement` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `262144` |
| `work_group_name` | `str` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `description` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `last_modified_time` | `datetime` | Optional | - |


# Example

```python
import dateutil.parser

from amazonathena.models.prepared_statement_1 import PreparedStatement1

prepared_statement_1 = PreparedStatement1(
    statement_name='StatementName8',
    query_statement='QueryStatement2',
    work_group_name='WorkGroupName2',
    description='Description6',
    last_modified_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z')
)
```



