# Batch Get Named Query Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkJhdGNoR2V0TmFtZWRRdWVyeU91dHB1dA


# Class Name

`BatchGetNamedQueryOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `named_queries` | [`List[NamedQuery]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/named-query.md) | Optional | - |
| `unprocessed_named_query_ids` | [`List[UnprocessedNamedQueryId]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/unprocessed-named-query-id.md) | Optional | - |


# Example

```python
from amazonathena.models.batch_get_named_query_output import BatchGetNamedQueryOutput
from amazonathena.models.named_query import NamedQuery
from amazonathena.models.unprocessed_named_query_id import UnprocessedNamedQueryId

batch_get_named_query_output = BatchGetNamedQueryOutput(
    named_queries=[
        NamedQuery(
            name='Name2',
            database='Database0',
            query_string='QueryString4',
            description='Description4',
            named_query_id='NamedQueryId0',
            work_group='WorkGroup4'
        ),
        NamedQuery(
            name='Name2',
            database='Database0',
            query_string='QueryString4',
            description='Description4',
            named_query_id='NamedQueryId0',
            work_group='WorkGroup4'
        ),
        NamedQuery(
            name='Name2',
            database='Database0',
            query_string='QueryString4',
            description='Description4',
            named_query_id='NamedQueryId0',
            work_group='WorkGroup4'
        )
    ],
    unprocessed_named_query_ids=[
        UnprocessedNamedQueryId(
            named_query_id='NamedQueryId4',
            error_code='ErrorCode6',
            error_message='ErrorMessage4'
        ),
        UnprocessedNamedQueryId(
            named_query_id='NamedQueryId4',
            error_code='ErrorCode6',
            error_message='ErrorMessage4'
        )
    ]
)
```



