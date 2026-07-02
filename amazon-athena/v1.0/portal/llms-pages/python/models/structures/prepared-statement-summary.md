# Prepared Statement Summary

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlByZXBhcmVkU3RhdGVtZW50U3VtbWFyeQ

The name and last modified time of the prepared statement.


# Class Name

`PreparedStatementSummary`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `statement_name` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256`, *Pattern*: `[a-zA-Z_][a-zA-Z0-9_@:]{1,256}` |
| `last_modified_time` | `datetime` | Optional | - |


# Example

```python
import dateutil.parser

from amazonathena.models.prepared_statement_summary import PreparedStatementSummary

prepared_statement_summary = PreparedStatementSummary(
    statement_name='StatementName0',
    last_modified_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z')
)
```



