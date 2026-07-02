# Query Execution

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlF1ZXJ5RXhlY3V0aW9u

Information about a single instance of a query execution.

*This model accepts additional fields of type Any.*


# Class Name

`QueryExecution`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `query_execution_id` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |
| `query` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `262144` |
| `statement_type` | [`StatementType1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/enumerations/statement-type-1.md) | Optional | - |
| `result_configuration` | [`ResultConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/result-configuration-1.md) | Optional | - |
| `result_reuse_configuration` | [`ResultReuseConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/result-reuse-configuration-1.md) | Optional | - |
| `query_execution_context` | [`QueryExecutionContext1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/query-execution-context-1.md) | Optional | - |
| `status` | [`Status`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/status.md) | Optional | - |
| `statistics` | [`Statistics`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/statistics.md) | Optional | - |
| `work_group` | `str` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `engine_version` | [`EngineVersion1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/engine-version-1.md) | Optional | - |
| `execution_parameters` | `List[str]` | Optional | **Constraints**: *Minimum Items*: `1`, *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `substatement_type` | `str` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.acl_configuration_1 import AclConfiguration1
from amazonathena.models.encryption_configuration_2 import EncryptionConfiguration2
from amazonathena.models.encryption_option_1 import EncryptionOption1
from amazonathena.models.query_execution import QueryExecution
from amazonathena.models.result_configuration_1 import ResultConfiguration1
from amazonathena.models.result_reuse_by_age_configuration_2 import ResultReuseByAgeConfiguration2
from amazonathena.models.result_reuse_configuration_1 import ResultReuseConfiguration1
from amazonathena.models.s_3_acl_option_1 import S3AclOption1
from amazonathena.models.statement_type_1 import StatementType1

query_execution = QueryExecution(
    query_execution_id='QueryExecutionId8',
    query='Query8',
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
)
```



