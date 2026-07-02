# Get Query Execution Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkdldFF1ZXJ5RXhlY3V0aW9uT3V0cHV0

*This model accepts additional fields of type Any.*


# Class Name

`GetQueryExecutionOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `query_execution` | [`QueryExecution1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/query-execution-1.md) | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.acl_configuration_1 import AclConfiguration1
from amazonathena.models.encryption_configuration_2 import EncryptionConfiguration2
from amazonathena.models.encryption_option_1 import EncryptionOption1
from amazonathena.models.get_query_execution_output import GetQueryExecutionOutput
from amazonathena.models.query_execution_1 import QueryExecution1
from amazonathena.models.result_configuration_1 import ResultConfiguration1
from amazonathena.models.result_reuse_by_age_configuration_2 import ResultReuseByAgeConfiguration2
from amazonathena.models.result_reuse_configuration_1 import ResultReuseConfiguration1
from amazonathena.models.s_3_acl_option_1 import S3AclOption1
from amazonathena.models.statement_type_1 import StatementType1

get_query_execution_output = GetQueryExecutionOutput(
    query_execution=QueryExecution1(
        query_execution_id='QueryExecutionId0',
        query='Query6',
        statement_type=StatementType1.DDL,
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
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



