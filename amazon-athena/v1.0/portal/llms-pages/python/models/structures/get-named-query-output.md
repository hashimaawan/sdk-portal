# Get Named Query Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkdldE5hbWVkUXVlcnlPdXRwdXQ


# Class Name

`GetNamedQueryOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `named_query` | [`NamedQuery1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/named-query-1.md) | Optional | - |


# Example

```python
from amazonathena.models.get_named_query_output import GetNamedQueryOutput
from amazonathena.models.named_query_1 import NamedQuery1

get_named_query_output = GetNamedQueryOutput(
    named_query=NamedQuery1(
        name='Name0',
        database='Database8',
        query_string='QueryString2',
        description='Description6',
        named_query_id='NamedQueryId2',
        work_group='WorkGroup2'
    )
)
```



