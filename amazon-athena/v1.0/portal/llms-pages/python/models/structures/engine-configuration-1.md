# Engine Configuration 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkVuZ2luZUNvbmZpZ3VyYXRpb24x

*This model accepts additional fields of type Any.*


# Class Name

`EngineConfiguration1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `coordinator_dpu_size` | `int` | Optional | **Constraints**: `>= 1`, `<= 1` |
| `max_concurrent_dpus` | `int` | Required | **Constraints**: `>= 2`, `<= 5000` |
| `default_executor_dpu_size` | `int` | Optional | **Constraints**: `>= 1`, `<= 1` |
| `additional_configs` | [`AdditionalConfigs`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/additional-configs.md) | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.additional_configs import AdditionalConfigs
from amazonathena.models.engine_configuration_1 import EngineConfiguration1

engine_configuration_1 = EngineConfiguration1(
    max_concurrent_dpus=56,
    coordinator_dpu_size=1,
    default_executor_dpu_size=1,
    additional_configs=AdditionalConfigs(
        additional_properties={
            'exampleAdditionalProperty': 'AdditionalConfigs_additionalProperties5'
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



