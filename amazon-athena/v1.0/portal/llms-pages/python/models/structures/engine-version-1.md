# Engine Version 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkVuZ2luZVZlcnNpb24x

*This model accepts additional fields of type Any.*


# Class Name

`EngineVersion1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `selected_engine_version` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `effective_engine_version` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.engine_version_1 import EngineVersion1

engine_version_1 = EngineVersion1(
    selected_engine_version='SelectedEngineVersion8',
    effective_engine_version='EffectiveEngineVersion8',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



