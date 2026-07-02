# Batch Get Query Execution Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkJhdGNoR2V0UXVlcnlFeGVjdXRpb25PdXRwdXQ


# Class Name

`BatchGetQueryExecutionOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `query_executions` | [`List[QueryExecution]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/query-execution.md) | Optional | - |
| `unprocessed_query_execution_ids` | [`List[UnprocessedQueryExecutionId]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/unprocessed-query-execution-id.md) | Optional | - |


# Example

```python
from amazonathena.models.acl_configuration_1 import AclConfiguration1
from amazonathena.models.batch_get_query_execution_output import BatchGetQueryExecutionOutput
from amazonathena.models.encryption_configuration_2 import EncryptionConfiguration2
from amazonathena.models.encryption_option_1_enum import EncryptionOption1Enum
from amazonathena.models.query_execution import QueryExecution
from amazonathena.models.result_configuration_1 import ResultConfiguration1
from amazonathena.models.result_reuse_by_age_configuration_2 import ResultReuseByAgeConfiguration2
from amazonathena.models.result_reuse_configuration_1 import ResultReuseConfiguration1
from amazonathena.models.s_3_acl_option_1_enum import S3AclOption1Enum
from amazonathena.models.statement_type_1_enum import StatementType1Enum
from amazonathena.models.unprocessed_query_execution_id import UnprocessedQueryExecutionId

batch_get_query_execution_output = BatchGetQueryExecutionOutput(
    query_executions=[
        QueryExecution(
            query_execution_id='QueryExecutionId6',
            query='Query0',
            statement_type=StatementType1Enum.UTILITY,
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
            result_reuse_configuration=ResultReuseConfiguration1(
                result_reuse_by_age_configuration=ResultReuseByAgeConfiguration2(
                    enabled=False,
                    max_age_in_minutes=26
                )
            )
        ),
        QueryExecution(
            query_execution_id='QueryExecutionId6',
            query='Query0',
            statement_type=StatementType1Enum.UTILITY,
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
            result_reuse_configuration=ResultReuseConfiguration1(
                result_reuse_by_age_configuration=ResultReuseByAgeConfiguration2(
                    enabled=False,
                    max_age_in_minutes=26
                )
            )
        )
    ],
    unprocessed_query_execution_ids=[
        UnprocessedQueryExecutionId(
            query_execution_id='QueryExecutionId6',
            error_code='ErrorCode2',
            error_message='ErrorMessage8'
        ),
        UnprocessedQueryExecutionId(
            query_execution_id='QueryExecutionId6',
            error_code='ErrorCode2',
            error_message='ErrorMessage8'
        ),
        UnprocessedQueryExecutionId(
            query_execution_id='QueryExecutionId6',
            error_code='ErrorCode2',
            error_message='ErrorMessage8'
        )
    ]
)
```



