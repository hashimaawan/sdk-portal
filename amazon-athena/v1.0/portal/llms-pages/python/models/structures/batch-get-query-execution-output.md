# Batch Get Query Execution Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkJhdGNoR2V0UXVlcnlFeGVjdXRpb25PdXRwdXQ

*This model accepts additional fields of type Any.*


# Class Name

`BatchGetQueryExecutionOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `query_executions` | [`List[QueryExecution]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/query-execution.md) | Optional | - |
| `unprocessed_query_execution_ids` | [`List[UnprocessedQueryExecutionId]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/unprocessed-query-execution-id.md) | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.acl_configuration_1 import AclConfiguration1
from amazonathena.models.batch_get_query_execution_output import BatchGetQueryExecutionOutput
from amazonathena.models.encryption_configuration_2 import EncryptionConfiguration2
from amazonathena.models.encryption_option_1 import EncryptionOption1
from amazonathena.models.query_execution import QueryExecution
from amazonathena.models.result_configuration_1 import ResultConfiguration1
from amazonathena.models.result_reuse_by_age_configuration_2 import ResultReuseByAgeConfiguration2
from amazonathena.models.result_reuse_configuration_1 import ResultReuseConfiguration1
from amazonathena.models.s_3_acl_option_1 import S3AclOption1
from amazonathena.models.statement_type_1 import StatementType1
from amazonathena.models.unprocessed_query_execution_id import UnprocessedQueryExecutionId

batch_get_query_execution_output = BatchGetQueryExecutionOutput(
    query_executions=[
        QueryExecution(
            query_execution_id='QueryExecutionId6',
            query='Query0',
            statement_type=StatementType1.UTILITY,
            result_configuration=ResultConfiguration1(
                output_location='OutputLocation0',
                encryption_configuration=EncryptionConfiguration2(
                    encryption_option=EncryptionOption1.SSE_S3,
                    kms_key='KmsKey6',
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                ),
                expected_bucket_owner='ExpectedBucketOwner0',
                acl_configuration=AclConfiguration1(
                    s_3_acl_option=S3AclOption1.BUCKET_OWNER_FULL_CONTROL,
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                ),
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            result_reuse_configuration=ResultReuseConfiguration1(
                result_reuse_by_age_configuration=ResultReuseByAgeConfiguration2(
                    enabled=False,
                    max_age_in_minutes=26,
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                ),
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        QueryExecution(
            query_execution_id='QueryExecutionId6',
            query='Query0',
            statement_type=StatementType1.UTILITY,
            result_configuration=ResultConfiguration1(
                output_location='OutputLocation0',
                encryption_configuration=EncryptionConfiguration2(
                    encryption_option=EncryptionOption1.SSE_S3,
                    kms_key='KmsKey6',
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                ),
                expected_bucket_owner='ExpectedBucketOwner0',
                acl_configuration=AclConfiguration1(
                    s_3_acl_option=S3AclOption1.BUCKET_OWNER_FULL_CONTROL,
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                ),
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            result_reuse_configuration=ResultReuseConfiguration1(
                result_reuse_by_age_configuration=ResultReuseByAgeConfiguration2(
                    enabled=False,
                    max_age_in_minutes=26,
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                ),
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    unprocessed_query_execution_ids=[
        UnprocessedQueryExecutionId(
            query_execution_id='QueryExecutionId6',
            error_code='ErrorCode2',
            error_message='ErrorMessage8',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        UnprocessedQueryExecutionId(
            query_execution_id='QueryExecutionId6',
            error_code='ErrorCode2',
            error_message='ErrorMessage8',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        UnprocessedQueryExecutionId(
            query_execution_id='QueryExecutionId6',
            error_code='ErrorCode2',
            error_message='ErrorMessage8',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



