# List Engine Versions Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkxpc3RFbmdpbmVWZXJzaW9uc091dHB1dA


# Class Name

`ListEngineVersionsOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `engine_versions` | [`List[EngineVersion]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/engine-version.md) | Optional | **Constraints**: *Minimum Items*: `0`, *Maximum Items*: `10` |
| `next_token` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |


# Example

```python
from amazonathena.models.engine_version import EngineVersion
from amazonathena.models.list_engine_versions_output import ListEngineVersionsOutput

list_engine_versions_output = ListEngineVersionsOutput(
    engine_versions=[
        EngineVersion(
            selected_engine_version='SelectedEngineVersion2',
            effective_engine_version='EffectiveEngineVersion2'
        ),
        EngineVersion(
            selected_engine_version='SelectedEngineVersion2',
            effective_engine_version='EffectiveEngineVersion2'
        )
    ],
    next_token='NextToken2'
)
```



