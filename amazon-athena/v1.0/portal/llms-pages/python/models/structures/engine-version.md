# Engine Version

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkVuZ2luZVZlcnNpb24

The Athena engine version for running queries, or the PySpark engine version for running sessions.

*This model accepts additional fields of type Any.*


# Class Name

`EngineVersion`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `selected_engine_version` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `effective_engine_version` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.engine_version import EngineVersion

engine_version = EngineVersion(
    selected_engine_version='SelectedEngineVersion4',
    effective_engine_version='EffectiveEngineVersion4',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



