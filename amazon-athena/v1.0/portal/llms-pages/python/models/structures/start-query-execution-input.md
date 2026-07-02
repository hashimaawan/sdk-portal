# Start Query Execution Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlN0YXJ0UXVlcnlFeGVjdXRpb25JbnB1dA


# Class Name

`StartQueryExecutionInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `query_string` | `str` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `262144` |
| `client_request_token` | `str` | Optional | **Constraints**: *Minimum Length*: `32`, *Maximum Length*: `128` |
| `query_execution_context` | [`QueryExecutionContext1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/query-execution-context-1.md) | Optional | - |
| `result_configuration` | [`ResultConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/result-configuration-1.md) | Optional | - |
| `work_group` | `str` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `execution_parameters` | `List[str]` | Optional | **Constraints**: *Minimum Items*: `1`, *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `result_reuse_configuration` | [`ResultReuseConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/result-reuse-configuration-1.md) | Optional | - |


# Example

```python
from amazonathena.models.acl_configuration_1 import AclConfiguration1
from amazonathena.models.encryption_configuration_2 import EncryptionConfiguration2
from amazonathena.models.encryption_option_1_enum import EncryptionOption1Enum
from amazonathena.models.query_execution_context_1 import QueryExecutionContext1
from amazonathena.models.result_configuration_1 import ResultConfiguration1
from amazonathena.models.s_3_acl_option_1_enum import S3AclOption1Enum
from amazonathena.models.start_query_execution_input import StartQueryExecutionInput

start_query_execution_input = StartQueryExecutionInput(
    query_string='QueryString6',
    client_request_token='ClientRequestToken8',
    query_execution_context=QueryExecutionContext1(
        database='Database4',
        catalog='Catalog0'
    ),
    result_configuration=ResultConfiguration1(
        output_location='OutputLocation0',
        encryption_configuration=EncryptionConfiguration2(
            encryption_option=EncryptionOption1Enum.SSE_S3,
            kms_key='KmsKey6'
        ),
        expected_bucket_owner='ExpectedBucketOwner0',
        acl_configuration=AclConfiguration1(
            s_3_acl_option=S3AclOption1Enum.BUCKET_OWNER_FULL_CONTROL
        )
    ),
    work_group='WorkGroup6',
    execution_parameters=[
        'ExecutionParameters8',
        'ExecutionParameters7'
    ]
)
```



